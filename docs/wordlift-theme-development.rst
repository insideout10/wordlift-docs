WordLift Theme Development
========

Who should read this 
_____________

This document is intended for Web Developers that would like to extend their themes to support WordLift's data model and features.

In the first paragraph we describe the WordLift data model, i.e. *how additional properties for entities are stored in WordPress*.

WordLift Data Model
_____________

1. WordLift Entities are **custom posts**;
2. Entity properties are managed as standard posts' metadata;
3. Entity types are managed through a `custom taxonomy <https://codex.wordpress.org/Taxonomies#Custom_Taxonomies>`_;
4. When a property references another entity:
	* Its value is the entity ID (if the entity is inside the same WordPress site),
	* Its value is the entity URI (if the entity is outside the WordPress site).
5. The 4Ws classification, i.e. the relationships among posts and entities, are stored in a custom table called *wl_relation_instances*.
6. WordLift's Topics are a `custom taxonomy <https://codex.wordpress.org/Taxonomies#Custom_Taxonomies>`_

Content Filtering - Available APIs
_____________

1. Standard WordPress methods (such as `get_posts <https://codex.wordpress.org/Template_Tags/get_posts>`_ and `get_post_meta <https://developer.wordpress.org/reference/functions/get_post_meta/>`_) can be used on entities;
2. `get_post_terms <https://codex.wordpress.org/Function_Reference/wp_get_post_terms>`_ can be used to extract topics from posts see the example below;

.. code-block:: php

	wp_get_post_terms( <post_id>, Wordlift_Topic_Taxonomy_Service::TAXONOMY_NAME, <args> )

3. WordLift's *Properties API* can be used to read/write entity properties using schema.org property names. See `here <https://github.com/insideout10/wordlift-plugin/blob/master/src/modules/core/wordlift_core_schema_api.php>`_; 
4. WordLift's *Relations API* can be used to access 4W relationships. See `here <https://github.com/insideout10/wordlift-plugin/blob/master/src/modules/core/wordlift_core_post_entity_relations.php>`_.

Personalization of Entity pages - Single Post  
_____________

Entities are configured in WordPress as `Custom Post Types <https://codex.wordpress.org/Post_Types#Custom_Post_Types>`_ and the post type is called **entity**. 

To personalise the design of entity pages the template file to be used is called `Single Post <https://developer.wordpress.org/themes/basics/template-hierarchy/#single-post>`_. 

Template files in WordPress are modular, reusable files, to create web pages on your web site. To learn more how to customize an existing WordPress theme or create a new one read the `template hirarchy page <https://developer.wordpress.org/themes/basics/template-hierarchy/>`_ on the WordPress website or visualise the `WordPress template hierarchy <https://wphierarchy.com/>`_.

.. note::

	When `articles or pages are turned into entities <https://wordlift.io/blog/en/wordlift-3-15/>`_ they mantain their existing post type.

To personalise the template based on the entity type use the following:

.. code-block:: php

	Wordlift_Entity_Type_Service::get_instance()->get( $post_id )

This will return:

.. code-block:: php

	 * @return array|null {
     * An array of type properties or null if no term is associated
     *
     * @type string css_class     The css class, e.g. `wl-thing`.
     * @type string uri           The schema.org class URI, e.g. `http://schema.org/Thing`.
     * @type array  same_as       An array of same as attributes.
     * @type array  custom_fields An array of custom fields.
     * @type array  linked_data   An array of {@link Wordlift_Sparql_Tuple_Rendition}.
     * }

Personalization of the Navigator Widget  
_____________

The `Navigator widget <discover.html#the-navigator-widget>`_ by default is wrapped in a `wl-navigator` class. You can style this class and the child element classes using CSS.

Optionally, while using the navigator, you can also specify a `template_id` to style a specific instance with its own template. 
The template can be written using `Mustache <https://github.com/Mustache/Mustache>`_: a framework-agnostic way to style web components.

Here's a sample code that you can use as reference:

.. code-block:: html

    <script id="wordlift_navigator_sidebar_template" type="text/mustache">
    {{#items}}
    <div class="related-articles__item">
    <a class="related-articles__img" href="{{post.permalink}}"><img src="{{{post.thumbnail}}}" alt="{{{post.title}}}" title="{{{post.title}}}"></a>
    <div class="related-articles__content">
        <h4 class="related-articles__title"><a href="{{post.permalink}}">{{{post.title}}}</a></h4>
    </div>
    </div>
    {{/items}}
    </script>

As a theme developer you have complete flexibility on both: the contents of these templates and the CSS styling. 
Read here the `parameters supported <shortcodes.html#navigator-widget>`_ by the Navigator widget.

Personalization of the Context Cards  
_____________

`Context Cards <discover.html#context-cards>`_ provide an immediate preview of an entity. If the entity has been annotated and, if links are active, WordLift will show a preview of the annotated entity.

By default context cards will show up on hovering if Links to Entity Pages are enabled. To disable context cards, add the following code to your theme:

.. code-block:: PHP
    add_filter('wl_context_cards_show' '__return_false')

The context card itself is wrapped within a class `wl-context-card` You can style this class and the child element classes using CSS. Other classes that you can use to style the context cards:

- `wl-context-card__image` - Image element
- `wl-context-card__description` - Wrapper element around complete description
- `wl-context-card__description__logo` - Publisher logo image element
- `wl-context-card__description__text` - Wrapper element around description text

Advanced Filters to override default behaviour
^^^^^^^^^^^^^^^

Javascript Filter `wl_context_cards_load_fn_supplier`
"""""""""""""""

This is a function supplier filter that the context card applies if provided. This filter can be used to supply a function that overrides the the default function that returns a fetch (or any other request library) promise. 

This filter receives two arguments: 

1. Endpoint of the context cards (`url`) 
2. DOM element that triggered the context card (`el`)

The filter is expected to return a fetch (or any other request library) promise with the desired request.

Here's a sample implementation of this filter:

.. code-block:: Javascript

    const settings = global["_wlEntityRedirectSettings"];

    addFilter("wl_context_cards_load_fn_supplier", "wordlift", (defaultFn) => {
        return (url, el) => {
            const enabled = el.getAttribute("data-entity-redirect-enabled");

            // If entity redirect isn't enabled for this target, then return the defaultFn.
            if ("true" !== enabled) return defaultFn(url, el);

            const join = -1 === url.indexOf("?") ? "?" : "&";
            // should load things
            const ids = el
                .getAttribute("data-id")
                .split(";")
                .map((s) => encodeURIComponent(s));

            const params =
                `${join}website=1&entity-redirect=true&id[]=` + ids.join("&id[]=");

            return fetch(`${settings.url}${params}`)
                .then((response) => response.json())
                .then((json) => {
                    // Return the JSON if it contains at least 2 elements (i.e. an entity and the web site).
                    if (1 < json.length) return json;

                    // Otherwise return the default function.
                    return defaultFn(url, el);
                });
        };
    });


PHP Filter `wl_anchor_data_attributes`
"""""""""""""""

This filter lets you add custom data attributes to `<a class="wl-anchor" />` links in the post. This received existing `attributes` and the `post_id`. Here's a sample implementation of this filter:

.. code-block:: PHP

    add_filter( 'wl_anchor_data_attributes', function ( $attributes, $post_id ) {

        return $attributes + array(
                'entity-redirect-enabled' =>
                    ( Wordlift_Entity_Redirect_Status::is_enabled( $post_id ) ? 'true' : 'false' )
            );
    }, 10, 2 );

