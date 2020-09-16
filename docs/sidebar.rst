Sidebar
===============

===============
Content Analysis and Disambiguation
===============

.. image:: /images/wordlift-content-analysis-disambiguation-start.png

Let's choose as relevant entity in this example *[Web]*, as the post is referring to the World Wide Web. As the entity type for *[Web]* is a `Thing` the entity appears under the *what* category. 

.. note::

    `Reconciling <key-concepts.html#reconciliation>`_ entities means **linking** the entity appearing in this text with its own equivalent on other sources (i.e. DBpedia or Freebase).

.. image:: /images/wordlift-edit-post-widget-05.png 

Using the `WordLift Edit Post Widget`_ you can now read the following parameters:

* **Entity Title** the name of the entity
* **Entity Category** the type of entity according to the `schema.org` vocabulary
* **Entity Description** the description of the entity

All parameters but the Title can be edited directly from the `WordLift Edit Post Widget`_

.. note::

	Data being used for the enrichments comes from openely avaialble sources
	like DBpedia that might contain misleading information that the editor can alwasy edit.

	Entity properties can also be edited clicking on the "open in vocabulary" link (see :doc:`edit-entity` page.)

Once you hit **Save** you are annotating this post which means adding a `semantic fingerprint <key-concepts.html#semantic-fingerprint>`_ to this piece of content.

In this post another important entity worth mentioning is the creator of the World Wide Web Sir Tim Berners-Lee.
The entity is properly identified as `Person` and all `Person` and `Organization` types are available under the *who* category.   

.. image:: /images/wordlift-content-analysis-disambiguation-berners-lee.png

.. note::

	Annotations are saved when a blog post or a page is published. Annotations and data related to each entity being annotated remain in *draft* untill the post is published. 

.. warning::

    When the text from the Visual Editor is edited or removed all annotations being saved are lost. WordLift stores the editor's selection of entities in the content of the Visual Editor. 
    
===============
Manual Entity Selection
===============
    
===============
Adding Entities
===============
    
The purpose of using WordLift is to (1) categorize your content, (2) help people find content of interest to them, and (3) help WordLift describe your contents in *machine-readable* format so that other computers can re-use it. 

In some cases key concepts that are important for (1), (2) and (3) are not automatically detected by WordLift and need to be taught by creating new entities.

.. note::

	A basic guideline for adding entity is: people should apply entities the same way a librarian would plausibly use tags to classify the content you're writing if it was a book. For some basic guidelines on when creating new entities `read here <faq.html#what-are-the-guidelines-for-creating-new-entities-to-annotate-a-blog-post-or-a-page>`_.

New entities being added will become part of the `WordLift vocabulary  <key-concepts.html#vocabulary>`_. 

Once an entity as been added to the vocabulary it will be automatically detected every-time you mention it again in your contents.

In our example one significant entity has not been detected and it is worth *teaching* it to WordLift. 

.. image:: /images/wordlift-content-analysis-new-entity-highlight.gif  

The entity is *[WordLift]* itself. To create a new entity simply highlight the text ``WordLift``, then click the button **Create New Entity** at the top of the `WordLift Edit Post Widget`_ and by clicking it you will be then able to edit the properties of the new entity. 

.. image:: /images/wordlift-content-analysis-new-entity-creation.png

Choose the category *Creative Work* (it also applies to *Software*), add a description and hit the "Save" button. Now the new entity will appear as `related entities <key-concepts.html#related-entities>`_  of the blog post along with *[Web]* and *[Tim Berners-Lee]*.   

.. image:: /images/wordlift-content-analysis-new-entity-creation2.png

.. warning::

    When creating a new entity over **an existing annotation**: a) remove the annotated entity, b) re-write the entity and c) create a new one (as described above). See animation below. 
 
.. image:: /images/wl-new-entity-specific-case.gif

===============
Updating and Linking Entities
===============


Updating the description
_____________

When we have something meanigful to say on a specific concept **we shall curate the information and edit the data that has been fetched automatically by WordLift** (*this will create our own version of Wikipedia*). 

Linking other entities
_____________

Entity pages can be annotated just like you would do with a blog posts. 

After saving the new description you wrote, WordLift will analyze the text and suggest related entities. You can now *link* an entity with other entities. WordLift will store these relationships between one entity and other entities in the `graph <key-concepts.html#knowledge-graph>`_ using the Dublin Core property ``dct:related``. This information will be used to infer new connections between the contents of the site. For more information on *entity linking* `read the faq <faq.html#when-should-i-link-one-entity-to-another>`_.   

..
	Entities being *linked* are listed as **Releated Entities** in the editing screen of the entity.

	.. image:: /images/wordlift-content-analysis-new-entity-related-entity.png
  
===============
Synonyms
===============

===============
Entity Types
===============
Here follows the list of properties that can be edited with WordLift for each entity type.

+--------------+--------------------+----------------------------+-------------------+
|     Type     |    Description     |         Properties         |     Schema.org    |
+==============+====================+============================+===================+
| Thing        |The most generic    |name,description,image,     | Thing_            |
|              |type of entity.     |type,URL,sameAs,            |                   |
|              |                    |additionalType.             |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Person       |A person.           |name,description,image,     | Person_           |
|              |                    |type,URL,sameAs,            |                   |
|              |                    |additionalType.             |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Place        |Entities            |name,description,image,     | Place_            |
|              |with a physical     |type,URL,sameAs,            |                   |
|              |extension.          |additionalType,geo.         |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Event        |An event happening  |name,description,image,     | Event_            |
|              |in a specific time  |type,URL,sameAs,            |                   |
|              |and location.       |additionalType,location,    |                   |
|              |                    |startDate,endDate,performer,|                   |
|              |                    |offers.                     |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Offer        |An offer.           |name,description,image,     | Offer_            |
|              |                    |availability,price,URL,     |                   |
|              |                    |priceCurrency,              |                   |
|              |                    |availabilityStarts,         |                   |
|              |                    |availabilityEnds,           |                   |
|              |                    |inventoryLevel,validFrom,   |                   |
|              |                    |priceValidUntil,itemOffered.|                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Organization |An organization.    |name,description,image,     | Organization_     |
|              |                    |type,URL,sameAs,            |                   |
|              |                    |additionalType,founder.     |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Local        |A physical business |name,description,image,     | LocalBusiness_    |
| business     |or branch of an     |type,URL,sameAs,address     |                   |
|              |organization.       |founder,geo.                |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Creative     |The most generic    |name,description,image,     | CreativeWork_     |
| Work	       |kind of Creative    |type,URL,sameAs,            |                   |
|              |Work(i.e. Software).|additionalType.             |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
|              |                    |                            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Recipe       |A food recipe.      |name,description,image,     | Recipe_           |
|              |                    |type,URL,sameAs,            |                   |
|              |                    |additionalType, cookTime,   |                   |
|              |                    |prepTime, totalTime,        |                   |
|              |                    |recipeCuisine,              |                   |
|              |                    |recipeIngredient,           |                   |
|              |                    |recipeInstructions,         |                   |
|              |                    |recipeYield,                |                   |
|              |                    |author, nutrition.calories. |                   |
+--------------+--------------------+----------------------------+-------------------+
