Analysis
========

Content Writing
_____________

To begin working with WordLift, once the plugin has been properly installed, we can simply begin writing
a blog post using the visual editor of WordPress.

WordLift adds to the visual editor its own menu. 

.. image:: /images/wordlift-menu.png

WordLift Menu
_____________

The menu has three functions:

* **Content analysis** (*cog icon*) 
		|	the text you're writing is sent to the cloud for being analysed.

* **New entity creation** (*pencil icon*)
		|	concepts that don't already exist can be created as part of your own `vocabulary <key-concepts.html#vocabulary>`_ by highlighting the text and clicking on this button. 

* **WordLift graphs** 
		|	a menu with different visualizations allows you to add `widgets <key-concepts.html#vocabulary>`_ in the page or in the sidebar.  

These functions are accessible when editing blog posts or pages.

.. image:: /images/wordlift-content-analysis-start.png

Analysing the text
_____________

To begin analysing the content I'm writing I need to click on the *cog icon*. 

By doing so I'm asking WordLift to enrich what I 
have written so far in the editor. The text is sent to the cloud and named entities are extracted.

.. image:: /images/wordlift-content-analysis-results.png

Entities being recognised are highlighted with a black underline. By clicking on each entity 
I can `reconcile <key-concepts.html#reconciliation>`_ it with the same entity in DBpedia or Freebase.

Reconciling entities
_____________

.. image:: /images/wordlift-content-analysis-disambiguation-start.png

I'm now choosing as relevant entity in my test *[Web]* as my post is referring to the World Wide Web.
And from the list of suggested entities I received from WordLift I choose to interlink the equivalent concept on DBpedia.

.. image:: /images/wordlift-content-analysis-disambiguation-selection.png

When doing so I can change the entity type for this entity using the drop-down menu. 

Type mismatch
--------------

In this specific case the associated type I receive is place (as seen from the pinpoint icon). 
Place as a type for the World WIde Web is misleading (the Web is rather a Creative Work). 

.. note::

	Data being used for the enrichments comes from openely avaialble sources
	like DBpedia that might contain misleading information like in this case. 

Changing type
--------------

To change the type of the entity I can use the drop-down menu and choose the proper type (Creative Work in this case).

.. image:: /images/wordlift-content-analysis-disambiguation-choosing-type.png

Once I select *Creative Work* I will hit the "save entity button" to create the entity *[Web]* as *Creative Work* and to add the `semantic fingerprint <key-concepts.html#semantic-fingerprint>`_ to my blog post.

.. image:: /images/wordlift-content-analysis-disambiguation-selection.png

.. note::

    `Reconciling <key-concepts.html#reconciliation>`_ entities means **linking** the entity appearing in my text with its own equivalent on other sources (i.e. DBpedia or Freebase).


In this initial text another important concept worth mentioning is the creator of the World Wide Web Sir Tim Berners-Lee.
The entity in this case is properly identified as Person (all Person type use in WordLift the person icon and the color pink) and information is sourced from DBpedia.   

.. image:: /images/wordlift-content-analysis-disambiguation-berners-lee.png

Proper type
--------------

As I don't need to change the type, I only need to click on the entity representing Tim and the annotation will be automatically saved once I published my post. 

 .. note::

	Annotations are saved when a blog post or a page is published. The annotations and the data related to each entity being annotated remain in *draft* untill the post or page is published. 

Once I click the "Publish" button to go live with my post, data is saved in WordPress and a new box appears in the editing screen showing the `related entities <key-concepts.html#related-entities>`_  of the blog post. 

.. image:: /images/wordlift-content-analysis-related-entities.png

You can now continue to the :doc:`editing-entity` page.
