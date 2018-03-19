Edit Entity
========
**WordLift** uses `entities <key-concepts.html#entity>`_ to annotate and organize blog posts and pages. 
All entities can be edited using the `WordLift Edit Post widget <analysis.html#wordLift-edit-post-widget>`_ or from the **Entity Page** itself. To access all entities or add a new entity click on the **Vocabolary** icon on the dashboard menu. 

.. image:: /images/wordlift-edit-entity-vocabulary.png

When annotating a post with an entity WordLift adds a link to the **entity page**. 
These links are useful for three reasons:

1. They allow users to navigate the website
2. They help establish information hierarchy using the network of entities
3. They could help spread link juice (ranking power) around the websites for better SEO.

Curating **entity pages** with WordLift is similar to writing an article on `Wikipedia <http://wikipedia.org>`_. These *entity posts* are useful for: 

* Providing contextual information to articles
* Aggregate all contents referring to the same entity  

..
	Referencing posts
	_____________

	Entities are saved in the WordPress databases as `custom posts <http://codex.wordpress.org/Post_Types>`_. Entities are related to blog posts and pages that are listed as **Referencing Posts** in the editing screen.  

	.. image:: /images/wordlift-edit-entity-referencing-posts.png

	In our case I can see that the entity *[Tim Berners-Lee]* is associated with the post *Hello World!*

Edit entity properties
_____________

The entity page provides the following set of properties that can be edited from the corresponding *meta box*:

	- **Name:** the title of the article 
	- **Description:** the body of the article
	- **Image:** the featured image of the article
	- **Entity Types:** the corresponding type (i.e. *Thing*, *Person*, *Place*, *Event*, *Organization*, *Creative Work*, ...) that can be managed via the *WordLift - Entity Type* box in the editing window
	- **Permalink:** the URL describing the entity
	- **Same-As:** the URLs of same entity on the different sources

.. image:: /images/wordlift-edit-entity-informations.png  

Entity types and properties Table
-------------------------------
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
|              |                    |priceCurrency,			     |                   |
|              |                    |availabilityStarts,         |                   |
|              |                    |availabilityEnds,           |                   |
|              |                    |inventoryLevel,validFrom,   |                   |
|              |                    |priceValidUntil,itemOffered |                   |
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


Edit an Event
-------------------------------
Events, occuring in a specific time are also entities. To personalise the *startDate*, *endDate* and *location* of an event you can use the **Event Properties** box.

.. image:: /images/wordlift-edit-entity-event.png

Edit a Place
-------------------------------
Places are also entities. To personalise the *geo coordinates* (longitude and latitude) of a place I can use the **Coordinates** box and either edit the *Latitude* and *Longitude* fields or simply place the pinpoint on the map.

.. image:: /images/wordlift-edit-entity-place.png

Edit a Recipe
-------------------------------
Recipes are also considered entities. To personalise *ingredients*, *cuisine*, *preparation time*, *cooking time*, *total time*, *number of portions*, *author* and *calories* I can edit the data using the Recipe meta boxes (make sure to choose the entity type *Recipe* in order to see these additional fields).   

.. image:: /images/wordlift-edit-entity-recipe-01.png

.. image:: /images/wordlift-edit-entity-recipe-02.png

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


The Faceted Search Widget
_____________

**Entity pages** can be used for helping users browse the content of your website. This is done using the **Faceted Search Widget**. 
The Widget can be added on the entity page using the **Faceted Search** option from the `Widgets Dropodown Menu <analysis.html#wordlift-widgets-menu>`_ 

.. image:: /images/wordlift-edit-entity-faceted-search-widget.png

Alternatively, the ``[wl_faceted_search]`` shortcode can be used.

* **Faceted Search** 
		|	Provides a faceted search user interface to help readers discover relevant articles using the network of entities.  

.. image:: /images/wordlift-edit-entity-faceted-search-widget-frontend.gif

The example above represents the widget displayed in the front-end. The reader can select multiple concepts and highlight the list of articles related to these concepts. 

Save data
_____________

In order to save the information on the entity press the "Publish" button.  
When making changes to an already existing entity press the "Update" button. In both cases data will be stored simultaneously on the WordPress site as well as in the `graph <key-concepts.html#knowledge-graph>`_.

You can now continue to the :doc:`publish` page.

.. _Thing: http://schema.org/Thing
.. _Person: http://schema.org/Person
.. _Place: http://schema.org/Place
.. _Event: http://schema.org/Event
.. _Organization: http://schema.org/Organization
.. _CreativeWork: http://schema.org/CreativeWork
.. _LocalBusiness: http://schema.org/LocalBusiness
.. _Recipe: http://schema.org/Recipe
.. _Offer: http://schema.org/Offer