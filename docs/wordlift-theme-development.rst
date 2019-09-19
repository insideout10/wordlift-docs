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

The Navigator widget by default is wrapped in a `wl-navigator` class. You can style this class and the child element classes using CSS.

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
