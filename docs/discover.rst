Discover
========
**WordLift** brings to the readers of your site multiple means of **content discovery**.

**WordLift** leverages on the semantic network of concepts (or `entities <key-concepts.html#entity>`_) being created to help users explore the content of your site. 

Using the `graph <key-concepts.html#knowledge-graph>`_ created by **WordLift** innovative ways of navigating the contents can be implemented (this is particularly true if you are a developer.)

**WordLift** helps users discover content in four different ways:

* **Links to Entity Pages**: placed on posts and pages and corresponding to the entities being annotated; 
* **Navigator Widget**: providing links to other blog posts related to the article  
* **Faceted Search Widget**: helping users discovering related content filtering by related entities. 
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

Users can choose multiple concepts to drill down the list of articles related to them. The default title for this widget - when it is added to a page - is "Related articles". This can be customised by adding any custom title in the shortcode. 

.. code-block:: html

	[wl_faceted_search title="this is my title"]  

The Chord Widget
_____________

The **Chord Widget** visualizes the relations between entities within a given article.

.. image:: /images/wordlift-shortcodes-chord.png

User might choose to navigate to an entity page or to another blog post.
