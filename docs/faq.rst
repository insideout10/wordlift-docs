FAQ
========

Why shall I use WordLift? 
_____________

The purpose of using WordLift is to (1) categorize your content, (2) help people find content of interest to them, and (3) help WordLift describe your contents in *machine-readable* format so that other computers can re-use it. 

What entity types are supported and how they map to Schema.org? 
_____________
*Thing*, *Person*, *Place*, *Event*, *Organization* and *Creative Work* are the supported types. 
Review the `Edit Entity page <edit-entity.html#entity-types-and-properties-table>`_ for more information.   

When should I create a new entity? 
_____________

You should create a new entity when this is directly relevant to the content you're writing and doesn't already exist. When an entity is properly recognised by WordLift you shall edit this entity rather then creating a new one. 

You can add as many entity as you like.

What are the guidelines for creating new entities to annotate a blog post or a page?
_____________

A basic guideline for adding a new entity is: 

	"*people should create entities that a librarian would plausibly use to classify the content as if it was a book.*"

The purpose of using WordLift is to (1) categorize your content, (2) help people find content of interest to them, and (3) help WordLift describe your contents in *machine-readable* format so that other computers can re-use it. 

In some cases key concepts that are important for (1), (2) and (3) are not automatically detected by WordLift and need to be taught. To teach WordLift new concepts a new entity shall be created.

.. note::

	When entities already exist we shall always avoid creating a new entity.

People should add entities that are accurate and directly relevant to the content they're writing, making it more likely that the content is seen by people who would be interested in it. 

A topic is directly relevant if the blog post (or page) is about the entity. If an article is not enriched with the main entity(ies) that it is about, people should add those entities.

Excessively broad entities should not be added to content. 

Content should not be overloaded with entities to increase its distribution online. As a general guideline, 8–16 entities should be adequate for most blog posts (based on the lenght of the article). If an article has too many entities it may be that some of the entities could be replaced with a single broader entity.

All entities shall be matched to the proper language of the content. 

When should I link one entity to another? 
_____________

By running the analysis on the property description text of an entity I can *link* it with other entities. WordLift will store these relationships between one entity and other entities in the `graph <key-concepts.html#knowledge-graph>`_ using the Dublin Core property ``dct:related``. This information will be used to suggest new connections between the contents of your site. Though is not mandatory creating links among relevant entities will create more structure for your contents. I should always link entities that can help other users discover relevant contents (i.e. the entity *[Berners-Lee]* shall be linked to entity *[Web]* as the two concepts are strictly related).

Even if these connections between different entities might already exists in the openely available sources we use like DBpedia and Freebase by creating them inside our own `graph <key-concepts.html#knowledge-graph>`_ we will be able to leverage on. 

What are the languages supported by WordLift? 
_____________

WordLift currently supports the following languages: English, 中文 (Chinese), Español (Spanish), Русский (Russian), Português (Portuguese), Deutsch (German), Italiano (Italian), Nederlands (Dutch), Svenska (Swedish) and Dansk (Danish). 

.. note::
	WordLift supports one language at the time. The main language of the website can be configured from the WordLift settings. 
	Review the `configuration settings <getting-started.html#configuration>`_ for more information. 

What are the datasets WordLift uses for named entity recognition? 
_____________

WordLift by default uses DBpedia and Freebase to detect and link named entities. With a custom configuration, the content analysis services provided by `Redlink <http://www.redlink.co>`_ and available via our professional services, can use any RDF-based `graph <key-concepts.html#knowledge-graph>`_. It is also possible to use *multiple graphs* for named entity recognition and `dereferencing <key-concepts.html#dereferencing-http-uris>`_. New entities being created with WordLift represent a custom vocabulary the analysis re-use for 