Discover
========
**WordLift** brings to the readers of your site multiple means of **content discovery**.

**WordLift** leverages on the semantic network of concepts (or `entities <key-concepts.html#entity>`_) being discovered to help users explore the contents of your site. 

Using the `graph <key-concepts.html#knowledge-graph>`_ created by **WordLift** innovative ways of navigating the contents of your site can be implemented (this is particularly true if you are a developer). 

**WordLift** out-of-the-box helps users discover contents in four different ways:

* **Links to Entity Pages**: these are places on posts and pages and corresponds to the concept being annotated, 
* **Navigator Widget**: it is designed to provide a quick overview of the article providing two types of links: 
** Links to Entity Pages descrbing the basic '*who*, *what*, *when* and *where*' of the article
** Links to other posts related to the article  
* **Faceted Search Widget**: from each Entity Pages presents all articles being related to that concept and helps users drill down on the list by filtering the interesting concepts. 
* **Chord Widget**: provides an overview of the network of concepts related to an article and links to other similar articles (articles that share the same entity) 

Links to Entity Pages
_____________
These **Entity Links** are useful for three reasons:

1. They allow users to navigate the website
2. They help establish information hierarchy using the network of entities
3. They could help spread link juice (ranking power) around the websites for better SEO.

.. image:: /images/wordlift-discover-entity-links.png

These links can be personalised using the CSS class ``wl-entity-page-link``. As seen in the example NASA is a link to an entity page (Mars is a normal link to an external webpage).

The Navigator Widget
_____________

The **Navigator Widget** provides content recommendations by presenting relevant links to other blog posts on your website. 

.. image:: /images/wordlift-discover-navigator.png

Each tile presents a **link to the entity** and a **link to a related post**.   

The Faceted Search Widget
_____________

Using the **Faceted Search Widget** readers, from each entity page, can find all related articles.  

.. image:: /images/wordlift-edit-entity-faceted-search-widget-frontend.gif

Users can choose multiple concepts to drill down the list of articles related to the entity. Entity page in the website navigation can be seen as an evolution of **tag pages** in WordPress.   

The Chord Widget
_____________

The **Chord Widget** visualizes the relations between entities, starting from the current post and all the entities being annotated.

.. image:: /images/wordlift-shortcodes-chord.png

