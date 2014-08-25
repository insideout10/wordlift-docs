Edit an Entity
========

Referencing posts
_____________

Entities are saved in the WordPress databases as `custom posts <http://codex.wordpress.org/Post_Types>`_. Entities are related to blog posts and pages that are listed as **Referencing Posts** in the editing screen.  

.. image:: /images/wordlift-edit-entity-referencing-posts.png

In our case I can see that the entity *[Tim Berners-Lee]* is associated with the post *Hello World!*.
The entity page provides the following set of properties that can be edited:

	- **Name:** the title of the article 
	- **Description:** the body of the article
	- **Image:** the featured image of the article
	- **Entity Type:** the corresponding type (i.e. *Thing*, *Person*, *Place*, *Event*, *Organization*, *Creative Work*, ...) that can be managed via the *Entity Type* box in the editing window
	- **Entity URL:** the URL describing the entity, the same-As label (the same entity on the different sources) and the entity-type-label (the types being associated on the external sources to the entity) that can be managed via the *Entity URL* box in the editing window.

Here follows the list of properties that can be edited with WordLift for each entity type.

.. image:: /images/wordlift-edit-entity-informations.png  

Entity types and properties Table
-------------------------------

+--------------+--------------------+----------------------------+-------------------+
|     Type     |    Description     |      Edit Properties       |     Schema.org    |
+==============+====================+============================+===================+
| Thing        |The most generic    | Name , Description , Image | `/Thing`_         |
|              |type of entity.     |, Type , URL , SameAs       |                   |
|              |                    |, additionalType            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Person       |A person.           | Name , Description , Image | `/Person`_        |
|              |                    |, Type , URL , SameAs       |                   |
|              |                    |, additionalType            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Place        |Entities            | Name , Description , Image | `/Place`_         |
|              |with a physical     |, Type , URL , SameAs       |                   |
|              |extension.			|, additionalType ,  Geo     |                   |
+--------------+--------------------+----------------------------+-------------------+
| Event        |An event happening  | Name , Description , Image | `/Event`_         |
|              |in a specific time  |, Type , URL , SameAs       |                   |
|              |and location.       |, additionalType ,  Geo ,   |                   |
|              |                    | startDate , endDate        |                   |
+--------------+--------------------+----------------------------+-------------------+
| Organization |An Organization.    | Name , Description , Image | `/Organization`_  |
|              |                    |, Type , URL , SameAs       |                   |
|              |                    |, additionalType            |                   |
+--------------+--------------------+----------------------------+-------------------+
| Creative     |The most generic    | Name , Description , Image | `/CreativeWork`_	 |
| Work		   |kind of Creative    |, Type , URL , SameAs       |                   |
|              |Work (i.e. Software)|, additionalType            |                   |
+--------------+--------------------+----------------------------+-------------------+

Updating properties
_____________

