Analysis
========

Content Writing
_____________

To begin working with WordLift, once the plugin has been properly installed, we can simply begin writing
a blog post using the visual editor of WordPress.

WordLift adds to the visual editor of WordPress its own menu. 

.. image:: /images/wordlift-menu.png

WordLift Menu
_____________

The menu has three functions:

* **Content analysis** (*cog icon*) 
		*the text you're writing is sent to the cloud for being analysed.
* **New entity creation** (*pencil icon*)
		*concepts that don't already exist can be created as part of your own `vocabulary <key-concepts.html#vocabulary>`_ by highlighting the text and clicking on this button. 
* **WordLift graphs** 
		*a menu with different visualizations allows you to add `widgets <key-concepts.html#vocabulary>`_ in the page or in the sidebar.  

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

.. image:: /images/wordlift-content-analysis-disambiguation-start.png

I'm now choosing as relevant entity in my test *[Web]* as my post is referring to the World Wide Web.
And from the list of suggested entities I received from WordLift I choose to interlink the equivalent concept on DBpedia.

.. image:: /images/wordlift-content-analysis-disambiguation-selection.png

When doing so I can choose the entity type for this entity using the drop-down menu. 

In this specific case the associated type I receive is place (as seen from the pinpoint icon). 
Place as a type for the World WIde Web is misleading (the Web is rather a Creative Work). 

.. note::

	Data being used for the enrichments comes from openely avaialble sources
	like DBpedia that might contain misleading information like in this case. 

.. image:: /images/wordlift-content-analysis-disambiguation-choosing-type.png

Once I select *Creative Work* I will hit the save entity button to create the entity *[Web]* as *Creative Work* and to add the `semantic fingerprint <key-concepts.html#semantic-fingerprint>`_ to my blog post.

.. image:: /images/wordlift-content-analysis-disambiguation-selection.png

.. note::

    `Reconciling <key-concepts.html#reconciliation>`_ entities means **linking** the entity appearing in my text with its own equivalent on other source (i.e. DBpedia or Freebase).
