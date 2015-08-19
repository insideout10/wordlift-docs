Analysis
========

**WordLift** adds semantic annotations and combines information publicly available as `linked open data <key-concepts.html#linked-open-data>`_ to organize and enrich contents. 

**WordLift** suggests to the content editor relevant fact-based information, images and links.

**WordLift** analyses articles using *Named Entity Recognition* (NER) and *Named Entity Disambiguation* (NED) to extract `Named Entities <key-concepts.html#entity>`_ from posts and pages. 

Entities, used for annotating contents, belong to different `knowledge graphs <key-concepts.html#knowledge-graph>`_ or `custom vocabularies <key-concepts.html#vocabulary>`_ including but not limited to DBpedia, GeoNames and Freebase.

WordLift creates and publishes annotations as `linked open data <key-concepts.html#linked-open-data>`_.

Content Writing
_____________

To start working with WordLift (once the plugin has been properly `installed <getting-started.html#installation>`_ and `configured <getting-started.html#configuration>`_) we can simply start writing a blog post using the `standard visual editor of WordPress <https://en.support.wordpress.com/visual-editor>`_.

WordLift adds to the visual editor the `WordLift Widgets Menu`_ to embed `widgets <key-concepts.html#widget>`_ in page. 

.. image:: /images/wordlift-menu.png

.. warning::

    WordLift works only with the standard **WordPress visual editor**. 
    WordLift cannot be used with *Visual Composer* (WorPress page builder) or any other customised page editor.

WordLift Widgets Menu
_____________

The menu lets you add four different `widgets <key-concepts.html#widget>`_ to your blog post. `widgets <key-concepts.html#widget>`_ provide a rich visual presentation of the entities populating the post and help readers find more relevant contents.  

.. note::
	As the site grows with new articles, new entities are created and contents are annotated, the graphical widgets automatically reflect the changes **without requiring any intervention from the editor**. This brings fresh new updates on your contents. 

The four `widgets <key-concepts.html#widget>`_ are:

* **Chord** 
		|	Visualizes the relationships between all entities starting from entities mentioned in the post.

* **Timeline** 
		|	Displays a navigable list of ordered entities of type *Event* mentioned in the post.  

* **GeoMap** 
		|	Displays all entities of type *Place* mentioned in the post on a map.  

* **Navigator** 
		|	Provides content recommendations by presenting relevant **internal** website links (links to other blog posts on the same website).  

Each widget has a corresponding shortcode; review the `widget shortcodes page <shortcodes.html#widget-shortcodes>`_ for more information on how this works.


Analysing the text
_____________

As I begin to write the content on the post, WordLift automatically starts analysing it. 

Once I hit the **Save Draft** button *for the first time*, `entities <key-concepts.html#entity>`_ are extracted and highlighted with a gray underline.

.. image:: /images/wordlift-content-analysis-results.png

By clicking on each entity I can `reconcile <key-concepts.html#reconciliation>`_ it with the same entity in DBpedia or Freebase using the `WordLift Edit Post widget`_. The entities that I choose will annotate this blog post.

.. note::

	Text annotation in WordLift is *semi-automatic*. `Entities <key-concepts.html#entity>`_ being extracted automatically are validated by the editor before being recorded.

With WordLift I can identify the basic '*who*, *what*, *when* and *where*' of an
article. I can also further structure the contextual information by creating new entities in the `custom vocabulary <key-concepts.html#vocabulary>`_. Annotations are added to posts and pages using the **WordLift Edit Post Widget**.


WordLift Edit Post Widget
--------------

Articles can be annotated in two ways: 

* **Top down**: entities are organized using the '*who*, *what*, *when* and *where*' categories **regardless of where each entity appears in the text**. When I choose an entity using the **top down** approach **all occurrences of that entity are annotated**. 

* **Bottom up**: entities are annotated and organized using the '*who*, *what*, *when* and *where*' categories **starting from each specific occurence of the entity in the text**. When I choose an entity using the **bottom up** approach **only the choosen occurrence of that entity is annotated**. 

Top down annotation
^^^^^^^^^^^^^^
The content editor, from the list of entities being detected in the text, uses these entities to describe his/her post without selecting any specific occurrence in the text. 
Entities being selected, in this case, describe the entire post (and not the single occurrence of the entity in the text).

.. image:: /images/wordlift-edit-post-widget-01.png 

Bottom up annotation
^^^^^^^^^^^^^^
The content editor has choosen the “Expo 2015” occurence in the text. In this case, this specific occurrence, is annotated with the entity "Expo 2015". 

.. image:: /images/wordlift-edit-post-widget-02.png


Edit Entity Properties
^^^^^^^^^^^^^^
The content editor is editing the main properties for the entity "Expo 2015" while writing the post. 
The complete list of properties can be edited from the :doc:`edit-entity` page.

.. image:: /images/wordlift-edit-post-widget-03.png

Image Suggestor
^^^^^^^^^^^^^^
.. image:: /images/wordlift-edit-post-widget-04.png 
Images for each entity appear in the WordLift Edit Post Widget and can be embedded in the visual editor. 

Reconciling entities
_____________

.. image:: /images/wordlift-content-analysis-disambiguation-start.png

I'm now choosing as relevant entity in my test *[Web]* as the post is referring to the World Wide Web. As the entity type for *[Web]* is `Thing` the entity appears under the *what* category. 

.. note::

    `Reconciling <key-concepts.html#reconciliation>`_ entities means **linking** the entity appearing in my text with its own equivalent on other sources (i.e. DBpedia or Freebase).

.. image:: /images/wordlift-edit-post-widget-05.png 

Using the `WordLift Edit Post Widget`_ I can now read the following parameters:

* **Entity Label** the name of the entity
* **Entity Type** the type of entity according to the `schema.org` vocabulary
* **Entity Description** the description of the entity
* **Entity Id** The URI of the entity (in this case the entity is coming from DBpedia)
* **Entity Same as** The URI of a corresponding entity (in this case the same entity is also present in Freebase)  

All parameters but **Entity Id** can be edited directly from the `WordLift Edit Post Widget`_

.. note::

	Data being used for the enrichments comes from openely avaialble sources
	like DBpedia that might contain misleading information that the editor can alwasy edit.

	Entity properties can also be edited from  

Once I hit **Save** on the `WordLift Edit Post Widget`_ I annotate this post (this means adding a `semantic fingerprint <key-concepts.html#semantic-fingerprint>`_ to this piece of content).

In this post another important concept worth mentioning is the creator of the World Wide Web Sir Tim Berners-Lee.
The entity is properly identified as `Person` and all `Person` and `Organization` types are available under the *who* category.   

.. image:: /images/wordlift-content-analysis-disambiguation-berners-lee.png

.. note::

	Annotations are saved when a blog post or a page is published. Annotations and data related to each entity being annotated remain in *draft* untill the post is published. 

.. warning::

    When the text from the Visual Editor is edited or removed all annotations being saved are lost. WordLift stores the editor's selection of entities in the content of the Visual Editor. 

Creating a new entity
_____________

The purpose of using WordLift is to (1) categorize your content, (2) help people find content of interest to them, and (3) help WordLift describe your contents in *machine-readable* format so that other computers can re-use it. 

In some cases key concepts that are important for (1), (2) and (3) are not automatically detected by WordLift and need to be taught by creating new entities.

.. note::

	A basic guideline for adding entity is: people should apply entities that a librarian would plausibly use to classify the content you're writing as if it was a book. For some basic guidelines on when creating new entities `read here <faq.html#what-are-the-guidelines-for-creating-new-entities-to-annotate-a-blog-post-or-a-page>`_.

New entities being added will become part of the `WordLift vocabulary  <key-concepts.html#vocabulary>`_. 

Once an entity as been added to the vocabulary it will be automatically detected every-time you mention it again in your contents.

In our example one significant entity has not been detected and it is worth *teaching* it to WordLift. 

.. image:: /images/wordlift-content-analysis-new-entity-highlight.gif  

The entity is infact *[WordLift]* itself. To create a new entity I will highlight the text ``WordLift``, the button **Add Entity** will appear in the `WordLift Edit Post Widget`_ and by clicking it I will be able to edit the properties of the new entity. 

.. image:: /images/wordlift-content-analysis-new-entity-creation.png

I will then choose the type Creative Work (it also applies to *Software*) and hit on the "Save the entity" button. Once I publish the post again the new entity will appear in the list of the `related entities <key-concepts.html#related-entities>`_  of the blog post along with *[Web]* and *[Tim Berners-Lee]*.   

You can now continue to the :doc:`edit-entity` page.
