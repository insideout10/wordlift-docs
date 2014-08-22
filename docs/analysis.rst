Analysis
========

Content Enrichment
_____________
To begin working with WordLift, once the plugin has been properly installed, we can simply begin writing
a blog post using the visual editor of WordPress.

WordLift adds to the visual editor of WordPress it's own menu. 

.. image:: /images/wordlift-menu.png

The menu has three functions:

* **Content analysis** (*cog icon*) 
* **New entity creation** (*pencil icon*)
* **WordLift graphs** 

These functions are accessible when editing blog posts or pages.

.. image:: /images/wordlift-content-analysis-start.png

To begin analysing the content I'm writing I need to click on the *cog icon*. 

By doing so I'm asking WordLift to enrich what I 
have written so far in the editor. The text is sent to the cloud and named entities are extracted.

.. image:: /images/wordlift-content-analysis-results.png

Entities being recognised are highlighted with a black underline. By clicking on each entity 
I can `reconciling <https://wordlift.readthedocs.org/en/latest/key-concepts.html#reconciliation>`_ it with the same entity in DBpedia or Freebase.

.. image:: /images/wordlift-content-analysis-disambiguation-start.png

I'm now choosing as relevant entity in my test *[Web]* as my post is referring to the World Wide Web.
And from the list of suggested entities I received from WordLift I choose to interlink the concept on DBpedia.

.. image:: /images/wordlift-content-analysis-disambiguation-selection.png

When doing I can choose the entity type for this entity using the drop-down menu

.. image:: /images/wordlift-content-analysis-disambiguation-choosing-type.png

As I choose to add this entity I am adding the `semantic fingerprint <https://wordlift.readthedocs.org/en/latest/key-concepts.html#semantic-fingerprint> for the entity *[Web]* to my blog post.

.. image:: /images/wordlift-content-analysis-disambiguation-selection.png

.. note::

    `Reconciling <https://wordlift.readthedocs.org/en/latest/key-concepts.html#reconciliation>`_ entities means **linking** the entity appearing in my text with its own equivalent on other source (i.e. DBpedia or Freebase).
