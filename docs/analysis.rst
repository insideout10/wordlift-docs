Analysis
========

WordLift adds semantic annotations and combines information publicly available as `linked open data <key-concepts.html#linked-open-data>`_ to enrich contents. 

WordLift suggests to the content editors relevant fact-based information, images and links.

WordLift analyses articles using Named Entity Recognition (NER) and Named Entity Disambiguation (NED). 

Entities, used in the annotation, may belong to different vocabularies or `knowledge graphs <key-concepts.html#knowledge-graph> including but not limited to DBpedia, GeoNames and Freebase.

WordLift provides UIs for creating and curating custom vocabularies that are published as `linked open data <key-concepts.html#linked-open-data>`_.

Content Writing
_____________

To start working with WordLift (once the plugin has been properly `installed <getting-started.html#installation>`_ and `configured <getting-started.html#configuration>`_) we can simply start writing a blog post using the `standard visual editor of WordPress <https://en.support.wordpress.com/visual-editor>`_.

WordLift adds to the visual editor a menu to add `widgets <key-concepts.html#vocabulary>`_ in the page or in the sidebar. 

.. image:: /images/wordlift-menu.png

.. warning::

    WordLift works only with the **WordPress visual editor**. 
    WordLift cannot be used with the Visual Composer (WorPress page builder) or any other customised page editor.

WordLift Widgets Menu
_____________

The menu lets you add four different `widgets <key-concepts.html#vocabulary>`_ to your blog post. `widgets <key-concepts.html#vocabulary>`_ provide a rich visual presentation of the entities populating the post and help readers find more relevant contents.  

.. note::
	As the blog grows and entities are created and mentioned, the widgets update their content without intervention from the editor.

The four `widgets <key-concepts.html#vocabulary>`_ are:

* **Chord** 
		|	Visualizes the relationships between all entities starting from the entities mentioned in the post.

* **Timeline** 
		|	Displays a navigable list of ordered *Event* entities mentioned in the post.  

* **GeoMap** 
		|	Displays *Place* entities on a map.  

* **Navigator** 
		|	Provides content recommendations by presenting relevant **internal** website links (links to other blognposts on the same website).  

Each widget has a corresponding shortcode; review the `widget shortcodes page <shortcodes.html#widget-shortcodes>`_ for more information on how this works.


Analysing the text
_____________

As I begin to write the content on the post, WordLift automatically start analysing it. 

As soon as I hit the **Save Draft** button in WordPress, WordLift enriches what I have written so far in the editor. 
In the background, the text is sent to the cloud and the `entities <key-concepts.html#entity>`_ are extracted and highlighted with a gray underline.

.. image:: /images/wordlift-content-analysis-results.png

By clicking on each entity I can `reconcile <key-concepts.html#reconciliation>`_ it with the same entity in DBpedia or Freebase using the `WordLift Edit Post widget <key-concepts.html#wordlift-edit-post-widget>`_. The entities that I will choose will be linked to this blog post. 

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

Once I click the "Publish" button of WordPress to go live with my post, data is saved in WordPress and a new box appears in the editing screen showing the `related entities <key-concepts.html#related-entities>`_  of the blog post. 

.. image:: /images/wordlift-content-analysis-related-entities.png

.. note::

    To replace entities being used in the annotation of the blog post after publishing we need to restart the analysis by clicking on the cog icon.

Creating a new entity
_____________

The purpose of using WordLift is to (1) categorize your content, (2) help people find content of interest to them, and (3) help WordLift describe your contents in *machine-readable* format so that other computers can re-use it. 

In some cases key concepts that are important for (1), (2) and (3) are not automatically detected by WordLift and need to be taught by creating new entities.

.. note::

	A basic guideline for adding entity is: people should apply entities that a librarian would plausibly use to classify the content you're writing as if it was a book. For some basic guidelines on when creating new entities `read here <faq.html#what-are-the-guidelines-for-creating-new-entities-to-annotate-a-blog-post-or-a-page>`_

New entities being added will become part of the `WordLift vocabulary  <key-concepts.html#vocabulary>`_. 

Once an entity as been added to the vocabulary it will be automatically detected every-time you mention it again in your contents.

In our example one significant entity has not been detected and it is worth *teaching* it to WordLift. 

.. image:: /images/wordlift-content-analysis-new-entity-highlight.png  

The entity is infact *[WordLift]* itself. To create a new entity I will highlight the text ``WordLift`` and click on the pencil icon "Insert entity".

.. image:: /images/wordlift-content-analysis-new-entity-creation.png

I will then choose the type Creative Work (it also applies to *Software*) and hit on the "Save the entity" button. Once I publish the post again the new entity will appear in the list of the `related entities <key-concepts.html#related-entities>`_  of the blog post along with *[Web]* and *[Tim Berners-Lee]*.   

You can now continue to the :doc:`edit-entity` page.
