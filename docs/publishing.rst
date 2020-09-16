Publishing
===============

===============
Rich Snippets
===============

===============
Linked Data
===============

===============
Widgets and Shortcodes
===============

Shortcodes
_________________

WordLift provides several useful shortcodes to provide enhanced visualizations on your web site.

Widgets
_________________

WordLift widgets can be inserted in a post or page to give a rich visual presentation of the entities populating the blog. As the blog grows and entities are created and mentioned, the widgets update their content without intervention from the editor.

Faceted Search
_________________


.. code-block:: html

    [wl_faceted_search]

The Faceted Search widget can be used on entity pages to display and filter the posts related to the current and other entities. It is useful for `content discovery <discover.html#the-navigator-widget>`_.

.. image:: /images/wordlift-edit-entity-faceted-search-widget-frontend.gif

Navigator
_________________


.. code-block:: html

    [wl_navigator]

The Navigator widget offers links to **semantic-related posts** in the blog. 
The search is made by considering the entities mentioned in the current post and by finding other blog posts that mentions the same entities. It is useful for `content discovery <discover.html#the-faceted-search-widget>`_.

.. image:: /images/wordlift-discover-navigator.png

Here follows the list of the supported parameters: 

title
    *(optional)* Title to be displayed above navigator. Defaults to 'Related articles'.

limit
    *(optional)* The total number of posts to display. Defaults to 4.

offset
    *(optional)* Offset for posts to display. It helps you break the list of recommended articles in different blocks (to add advertising and/or CTAs). Defaults to 0. Defaults to 4.

template_id 
    *(optional)* The id of the script element which has mustache template. For example if the template is in `<script id="wordlift_navigator_sidebar_template" type="text/mustache">...</script>` then `template_id` would be `wordlift_navigator_sidebar_template`.

post_id
    *(optional)* The post ID of a post of which navigator you want to display. Defaults to the current post. This is helpful if you want to display the navigator of post 'A' on post 'B' or add the navigator shortcode for a specific post in a non-post page.

uniqid
    *(optional)* The Unique ID for the navigator. This can be used to style or to apply navigator filters that are specific to an instance of the navigator (instead of acting on multiple navigators).

Here is a sample code for personalizing the template to be used as reference:

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

The filters available for the navigator widget are:

- `wl_navigator_data_post`: Gets each navigator post item, post ID and uniqid. Returns the customized post item.
- `wl_navigator_data_entity`: Gets each entity post item, post ID and uniqid. Returns the customized entity item.
- `wl_navigator_data_placeholder`: Gets the complete result array and uniqid. Returns the customized result array. Can be used to seed navigator with placeholder 

Chord
_________________


.. code-block:: html

    [wl_chord width=... height=... main_color=... depth=... global=...]
    
.. image:: /images/wordlift-shortcodes-chord.png
The Chord widget visualizes relations between entities, starting from the current post and the entities mentioned in it.

width
    *(optional)* Width of the chord. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the chord. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

main_color
    *(optional)* The chord's *base* color.

depth
    *(optional)* Maximum distance to travel in the entity graph in order to populate the chord. A small number limits the exploration of the main entity.

global
    *(optional)* When *global=true* the main entity of the chord is not the current post, but the most mentioned entity in the latest posts.

Geomap
_________________


.. code-block:: html

    [wl_geomap width=... height=... global=...]
    
.. image:: /images/wordlift-shortcodes-geomap.png    
The Geomap widget displays "Place" entities on a map. Each Place has its own marker with a popup containing a thumbnail and links of the place. Here are the parameters:
    
width
    *(optional)* Width of the geomap. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the geomap. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

global
    *(optional)* By default the geomap displays places mentioned in the current post. When *global=true* the geomap displays all places mentioned in the blog.
    
Timeline
_________________

.. code-block:: html
    
    [wl_timeline width=... height=... global=...]
    
.. image:: /images/wordlift-shortcodes-timeline.png
The Timeline widget displays a navigable list of chronologically ordered Event entities. The window on top shows details of the selected Events.
Here follows the list of the supported parameters:

width
    *(optional)* Width of the timeline. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the timeline. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

global
    *(optional)* By default the timeline displays events (or events related to places) mentioned in the current post. When *global=true* the timeline displays events mentioned in the latest posts.

display_images_as
    *(optional)* When *display_images_as='background'* the timeline displays for each event the featured image of the entity as background.

excerpt_length
    *(optional)* Allows you to set the number of words that appear in the the excerpts of the timeline. 

.. note::
        When you create a timeline with WordLift you can pass in the shortcode optional parameters to set a variety of presentation options. These are derived from the TimelineJS library `read more here <https://timeline.knightlab.com/docs/options.html>`_.


Entity Cloud
_________________

.. code-block:: html

    [wl_cloud]

The **WordLift Entities Cloud Widget** is also available as a shortcode. The widget displays entities related to the current post/entity in a tag cloud.

.. image:: /images/wordlift-entities-cloud-widget.png

Glossary
_________________

.. code-block:: html

    [wl_vocabulary limit=... type=... orderby=...]  

The **Glossary** is a site-wide Widget that displays all the entities in alphabetical order. Here you can see an example of the `Semantic SEO Glossary <https://wordlift.io/blog/en/glossary>`_ 

.. image:: /images/wordlift-discover-vocabulary.gif

By default the widget takes into account the latest 100 entities from all types (i.e. Person, Place, Organization, ...). 
The following paramenters can be used to personalise the entities beind displayed in the vocabulary:

limit 
    the total number of entities to displaye (*100* is the defualt value). Use `-1` to remove the limit.

type
    the type of entities to display (*all* is the default value). Use `Person`to display only entities of type Person.     

orderby
    the selection is by default related to the alphabetical order (*title* is the default value). Selected entities can be ordered using different parameters. `Read more here <https://developer.wordpress.org/reference/classes/WP_Query/parse_query/>`_

.. _PHP date: http://php.net/manual/en/function.date.php
.. _PHP DateInterval format: http://php.net/manual/en/dateinterval.format.php


