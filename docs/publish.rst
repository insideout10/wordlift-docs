Publish
========

Publish Entity
_____________

Entities when saved are created as `custom posts` in the local WordPress installation and are accessible from the `WordLift vocabulary <key-concepts.html#vocabulary>`_. 

.. note::

	The URL for an entity page is as follows::
		http://*<name-of-your-WordPress-server>*/?entity=<*name-of-the–entity*>


The Faceted Search Widget 
-------------------------------
**Entity pages** can be used for helping users browse the content of your website. This is done using the **Faceted Search Widget**. 
The Widget can be added on the entity page using the **Faceted Search** option from the `WordLift Widgets Menu <analysis.html#wordlift-widgets-menu>`_ 

.. image:: /images/wordlift-edit-entity-faceted-search-widget.png

Alternatively, the `[wl_faceted_search]` shortcode can be used.

* **Faceted Search** 
		|	Provides a faceted search user interface to help readers find relevant articles using the network of entities.  

.. image:: /images/wordlift-edit-entity-faceted-search-widget-frontend.gif

Metadata being added to Entity pages 
-------------------------------


RDF representation of the Entity 
-------------------------------
By clicking on the **View on Linked Data** button (right after the *Permalink* in the editor) the **RDF representation of the entity** is displayed using `LodView <http://lodview.it/>`_. 

.. image:: /images/wordlift-publish-entity-lodview.png

In this example I can see the relation being created between the entity *[Mars]* and the entity *[Solar System]* (`dcterms:relation`). This relation has been created from the :doc:`edit-entity` page by annotating the description of the entity. 

.. image:: /images/wordlift-publish-entity-lodlive.png

I can also see (in this last image using `LodLive <http://lodlive.it/>`_) the `sameAs` attributes.  


Publish Post/Page
_____________
Posts and Pages with **WordLift** are annotated using the `schema.org` vocabulary. 
The *schema markup* is a code (semantic vocabulary) to help search engines return more informative results for their users.

Metadata being added to Post/Page 
-------------------------------
By clicking on the **Test Google Rich Snippets** button (right after the *Permalink* in the editor) we can see the list of entities being added to the content.

.. image:: /images/wordlift-publish-structured-data-testing.png 

In this example we're telling search engines that this post is relevant for search around the concept of *[Solar System]* (here represented as *Place*).   

RDF representation of the Post/Page 
-------------------------------
By clicking on the **View on Linked Data** button (right after the *Permalink* in the editor) the **RDF representation of the post** is displayed using `LodView <http://lodview.it/>`_. 


You can now continue to the :doc:`discover` page.
