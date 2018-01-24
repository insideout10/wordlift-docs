Discover
========
**WordLift** brings to the readers of your site multiple means of **content discovery**.

**WordLift** leverages on the semantic network of concepts (or `entities <key-concepts.html#entity>`_) being created to help users explore the content of your site. 

Using the `graph <key-concepts.html#knowledge-graph>`_ created by **WordLift** innovative ways of navigating the contents can be implemented (this is particularly true if you are a developer.)

**WordLift** helps users discover content in four different ways:

* **Links to Entity Pages**: placed on posts and pages and corresponding to the entities being annotated; 
* **Navigator Widget**: providing links to other blog posts related to the article;  
* **Faceted Search Widget**: helping users discovering related content filtering by related entities; 
* **Timeline Widget**: creating beautiful and interactive timelines; 
* **Chord Widget**: providing a quick overview of the network of concepts related to an article and links to other similar articles sharing the same entities.

Links to Entity Pages
_____________
**Entity Links** are useful for three reasons:

1. They allow users to navigate the website
2. They help establish information hierarchy using the network of entities
3. They could help spread link juice (ranking power) around the websites for better SEO.

.. image:: /images/wordlift-discover-entity-links.png

These links can be personalised using the CSS class ``wl-entity-page-link``. As seen in the example NASA is a link to an entity page while Mars is a normal link to an external webpage.

The Navigator Widget
_____________

The **Navigator Widget** provides content recommendations by presenting relevant links to other blog posts on your website. 

.. image:: /images/wordlift-discover-navigator.png

Each tile presents a **link to an entity** (*[NASA]* and *[Earth]* in this example) and/or a **link to a related post**.   

The Faceted Search Widget
_____________

Using the **Faceted Search Widget** readers, selecting concepts they are interested in, can find all related articles.  

.. image:: /images/wordlift-edit-entity-faceted-search-widget-frontend.gif

Users can choose multiple concepts to drill down the list of articles related to them. 

The default title for this widget - when it is added to a page - is "**Related articles**". This title be customised by adding the new title in the shortcode as shown in the example below. 

.. code-block:: html

	[wl_faceted_search title="this is my new title"]  

The Timeline Widget
_____________

**WordLift** uses the powerful `TimelineJS <https://timeline.knightlab.com/>`_ to create beautiful, interactive timelines. 
The timeline widget in **WordLift** uses nothing more than `entities of type event <edit-entity.html#edit-an-event>`_ mentioned and annotated in the article. 

`Entities of type event <edit-entity.html#edit-an-event>`_ can be linked to entities of type place via the property *location* (this describe where the event is taking place). If a place is mentioned in the article and it is linked to an event the timeline will display this event also.

.. image:: /images/wordlift-shortcodes-timeline.png

.. note::
        In order for an event to appear in the timeline the event property *startDate* shall be present as illustrated `here <edit-entity.html#edit-an-event>`_.

.. note::


It is possible to personalise the layout of the timeline using any of `the presentation options of TimelineJS <https://timeline.knightlab.com/docs/options.html>`_ plus three additional parameters provided by WordLift:

1. **excerpt_length** let's you control the lenght of text (in number of characters) displayed for each event (this corresponds to the description of the entity)
2. **display_images_as** the default value is *media*, alternatively you can use *background* and the fetured image of the entity will be used as background    
3. **global** when set to *true* the timeline displays events mentioned in the latest posts (no need to add mentions to places or events in this case).

.. note::
        When you create a timeline with WordLift you can pass in the shortcode optional parameters to set a variety of presentation options. These are derived from the TimelineJS library `read more here <https://timeline.knightlab.com/docs/options.html>`_.


.. code-block:: html

	[wl_timeline display_images_as='background' height='600px' excerpt_length=25 global='true']  

This shortcode above produces the following result: 

.. image:: /images/wordlift-shortcodes-timeline-02.png


The Chord Widget
_____________

The **Chord Widget** visualizes the relations between entities within a given article.

.. image:: /images/wordlift-shortcodes-chord.png

User might choose to navigate to an entity page or to another blog post.


The WordLift Entities Cloud WordPress Widget
_____________

The **WordLift Entities Cloud WordPress Widget** is a site-wide Widget and a shortcode that displays entities related to the current post/entity in a tag cloud. WordPress Widgets like this one add content and features to your Sidebars. To add the widget:

1. Go to **Appearance > Customize** in the WordPress Administration Screens.
2. Click the **Widget** menu in the Theme Customizer to access to the Widget Customize Screen.

.. image:: /images/wordlift-entities-cloud-widget.png

It is possible, just like for other WordPress Widgets to personalize the title of the Widget. This widget can also be added to an article or a page with the following shortcode: 

.. code-block:: html

	[wl_cloud]  


The Timeline WordPress Widget
_____________

The **Timeline WordPress Widget** is a site-wide Widget that displays events being saved as entities (type event) using the `interactive timeline <discover.html#the-timeline-widget>`_.

.. image:: /images/wordlift-timeline-wordpress-widget.png

The Glossary Widget
_____________

The **Glossary** is a site-wide Widget that displays all the entities in alphabetical order.

.. code-block:: html

    [wl_vocabulary limit=... type=... orderby=...]  

By default the widget takes into account the latest 100 entities from all types (i.e. Person, Place, Organization, ...). 
The following paramenters can be used to personalise the entities beind displayed in the vocabulary:

1. **limit** the total number of entities to displaye (*100* is the defualt value). Use `-1` to remove the limit.
2. **type** the type of entities to display (*all* is the default value). Use `Person`to display only entities of type Person.     
3. **orderby** the selection is by default related to the alphabetical order (*title* is the default value). Selected entities can be ordered using different parameters. `Read more here <https://developer.wordpress.org/reference/classes/WP_Query/parse_query/>`_


.. image:: /images/wordlift-discover-vocabulary.gif

Here you can see an example of the `Semantic SEO Glossary <https://wordlift.io/blog/en/glossary>`_.
