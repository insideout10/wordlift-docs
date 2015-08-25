Publish
========

Publish Entity
_____________

Entities when saved are created as `custom posts` in the local WordPress installation and are accessible from the `WordLift vocabulary <key-concepts.html#vocabulary>`_. 

.. note::

	The URL for an entity page is as follows::
		http://*<name-of-your-WordPress-server>*/?entity=<*name-of-the–entity*>


Metadata being added to Entity pages 
-------------------------------


RDF representation of the Entity 
-------------------------------
By clicking on the **View on Linked Data** button (right after the *Permalink* in the editor) the **RDF representation of the entity** is displayed using `LodView <http://lodview.it/>`_. 

.. image:: /images/wordlift-publish-entity-view-linked-data.png

.. image:: /images/wordlift-publish-entity-lodview.png

In this example I can see the relation being created between the entity *[Mars]* and the entity *[Solar System]* (``dcterms:relation``). This relation has been created from the `edit entity page <edit-entity.html#linking-other-entities>`_ page by annotating the description of the entity. 

.. image:: /images/wordlift-publish-entity-lodlive.png

I can also see (in this last image using `LodLive <http://lodlive.it/>`_) the `sameAs` attributes.  


Publish Post/Page
_____________
Posts and Pages with **WordLift** are annotated using the `schema.org` vocabulary. 
The *schema markup* is a code (semantic vocabulary) to help search engines return more informative results for their users.

Metadata being added to Post/Page 
-------------------------------
By clicking on the **Test Google Rich Snippets** button (right after the *Permalink* in the editor) we can see the list of entities being added to the content from the **Google Structured Data Testing Tool**.

.. image:: /images/wordlift-publish-post-test-structured-data.png

.. image:: /images/wordlift-publish-structured-data-testing.png 

In this example we're telling search engines that this post could be relevant for searches related to the *[Solar System]*.   

RDF representation of the Post/Page 
-------------------------------
By clicking on the **View on Linked Data** button (right after the *Permalink* in the editor) the **RDF representation of the post** is displayed using `LodView <http://lodview.it/>`_. 

As of today, the data being represented in RDF for each post or page include: 

* schema-org:**datePublished**
* schema-org:**dateModified**
* schema-org:**interactionCount**
* rdfs:**label**
* rdf:**type**
* schema-org:**url**
* dcterms:**references**
* schema-org:**author**

.. image:: /images/wordlift-publish-post-lodview.png

.. note::

	In the RDF representation of the posts I can find all entities related to a post (or a page) by looking at the ``dcterms:references`` attribute

The attributes describing the posts can be browsed. In this example by clicking on the entity *[Solar System]* I will be able (directly from `LodView <http://lodview.it/>`_) to consult and read the data publish on that entity by **WordLift**.  

You can now continue to the :doc:`discover` page.
