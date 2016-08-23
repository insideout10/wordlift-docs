FAQ
========

Why shall I use WordLift? 
_____________

Throwing content online without context and analysis simply doesn’t work when the focus for digital news is on *interactivity*, *engagement* and *community*. 
**WordLift** organizes knowledge, **reducing the complexity of content management and digital marketing operations**, letting bloggers and site owner **focus on stories and communities**. It offers meaningful *cross-media discovery* and *recommendations* that **increases content quality, exposure, trustworthiness and readership engagement**. 
**WordLift** also publishes *linked data* as a new way to syndicate content and create new business models.

Why is it important to organize my content and publish it as Linked Data?
_____________

Organizing web content around concepts rather than traditional web pages helps both users and machines finding and accessing it, improves **navigation**, **content re-use**, **content repurposing** and **search engine rankings**. 
**Enriching content** with *contextual information*, *links* and *media*, from custom vocabularies and/or the wealth of **open data** available on the web, brings the user experience to a new level of engagement. 
Structuring content with **richer metadata** and publishing it as `linked data <http://docs.wordlift.it/en/latest/key-concepts.html#linked-open-data>`_ makes it **discoverable and searchable**, providing new ways of reaching targets.

Who is WordLift for?
_____________

**WordLift** is for all *bloggers*, *journalists*, and *content creators* publishing and fighting for readers’ attention on the web.  
Online publishers and broadcasters like BBC, Financial Times, New York Times, Washington Post, Reuters and Associated Press are investing in **dynamic semantic publishing** and use `linked open data <key-concepts.html#linked-open-data>`_ to organise their news portals and content applications. 

**WordLift** democratizes the field, bringing to the hands of all web content creators and publishers the technology to efficiently organize their content creation process and reach their tribes. 

**WordLift** helps you create your own **knowledge graph** using the same technologies that giants like *Facebook*, *IBM* and *Google* are using to monetise their vast amount of data.

How does it work?
_____________

.. note::

	To know more about how **WordLift** works, please `watch the step by step video tutorials <https://wordlift.io/#how-it-works>`_ on our `website <https://wordlift.io>`_. 

**WordLift** works in subsequent stages. The first step provides a full text analysis and suggests entities and relationships to the user, classifying contents according to concepts stored in the *semantic graph* (DBpedia, Wikidata, GeoNames, etc.) and using schema.org vocabulary. Textual contents are structured: they can now be processed by machines and be connected to other datasets. Users can also create new entities, to complement the entities suggested automatically and form a proprietary vocabulary, according to the editorial plans. 

**WordLift** also assists writers suggesting links, media and providing a set of powerful visualization widgets to connect and recommend alternative content. 

Finally **WordLift** provides means to record all these relationships in a graph database combining structured, semistructured and unstructured data, which allows queries like *“find all contents related to concept_y and relevant for target_z”*. 

Why is WordLift innovative
_____________

**WordLift** is **first-to-market** following a **“content organization” approach** which allows the classification and direct exploitation of proprietary content and structured metadata. 
**Wordlift** helps publishers create their **knowledge graph**, *exploit it* and *monetize it*. 
Finally **WordLift** complements the offer of plug-ins such as *SEO Ultimate* or *Yoast* **automatically adding schema.org mark-ups** to content, allowing search engines to properly index pages, increasing traffic from organic searches.

Who owns the structured metadata created with WordLift?
_____________ 

**You do!** We believe content creators should retain the commercial value of their content and all the data they create, and exploit it through new business models based on **content syndication**, **data-as-a-service** and a stronger **relationship with their audience**. 
This is stated in our `Terms of Service <https://wordlift.io/terms-of-service>`_ and our `Privacy Policy <https://wordlift.io/privacy/>`_ as well!

What happens if I stop using WordLift? 
_____________

1. If you stop paying for your subscription, but keep the plugin on your site, all the entities, metadata and pages you created with wordlift will still be available on your site - you won't be able to update it any longer, but they will still work just fine as they were at the moment you removed the key. The data you’ve created belongs to you and you can always request to us a data dump that is available in various machine-readable formats.

2. if you deactivate the plugin instead, the vocabulary (metadata, entity and pages) will disappear from your dashboard, but everything you created is stored in your website Database in WordPress, and you will be able to download it, transfer it or re-activate it again anytime from the plugin menu. 

3. Turning off WordLift on our side, it would be like turning off all the keys and un-publish all the linked data you’ve created, not the plug-in itself, so it will be like #1 - you could get the data back from us and re-publish it as `linked data <http://docs.wordlift.it/en/latest/key-concepts.html#linked-open-data>`_ on your own infrastructure.

4. WordLift's technology is entirely open source: it takes development skills, infrastructure and some wisdom to nicely bring all the pieces together without our support.

5. Your vocabulary (article metadata and entities) are published as `linked data <http://docs.wordlift.it/en/latest/key-concepts.html#linked-open-data>`_ and you can always request a data dump in any of the following formats: RDF/XML, Turtle, N3, JSON-LD.


What is content enrichment? 
_____________

Content enrichment is a processes used to refine and improve textual content by embedding structured data (*metadata*) on web pages. This *metadata* is made available to search engines and other data consumers. 

What entity types are supported and how they map to Schema.org? 
_____________
*Thing*, *Person*, *Place*, *Event*, *Organization*, *LocalBusiness* and *Creative Work* are the supported types. 
Review the `Edit Entity page <edit-entity.html#entity-types-and-properties-table>`_ for more information.   

When should I create a new entity? 
_____________

You should create a new entity when this is directly relevant to the content you're writing and it doesn't already exist. When an entity is properly recognised by WordLift you shall edit this entity rather then creating a new one. 

You can add as many entities as you like.

What are the guidelines for creating new entities to annotate a blog post or a page?
_____________

A basic guideline for adding a new entity is: 

	"*people should create entities that a librarian would plausibly use to classify the content as if it was a book.*"

The purpose of using WordLift is to (1) categorize your content, (2) help people find content of interest to them, and (3) help WordLift describe your contents in *machine-readable* format so that other computers can re-use it. 

In some cases key concepts that are important for (1), (2) and (3) are not automatically detected by WordLift and need to be taught. To teach WordLift new concepts a new entity shall be created.

.. note::

	When entities already exist we shall always avoid creating a new entity.

People should add entities that are accurate and directly relevant to the content they're writing. 

Excessively broad entities should not be added to content. 

Content should not be overloaded with entities to increase its distribution online. As a general guideline, 8–16 entities should be adequate for most blog posts (based on the lenght of the article). If an article has too many entities it may be that some of the entities could be replaced with a single broader entity.

All entities shall be matched to the proper language of the content. 

What factors determine Wordlift's rating of an entity?
_____________

The entity rating in WordLift takes under account the following factors:

- Every entity should be linked to one or more related posts. 
- Every entity should have its own description. 
- Every entity should link to other entities - when we select other entities to enrich the description of an entity we create relationships in the site's `knowledge graph <key-concepts.html#knowledge-graph>`_.
- Entities, just like any post in WordPress, can be kept as draft. Only when we publish them they become available in the analysis and we can use them to classify our contents.
- Entities shall have a feautured image. When we add a featured image to an entity we’re adding the `schema-org:image` attribute to it.
- Every entity (unless we’re creating something completely new) should be interlinked with the same entity containedin at least one other dataset. This is called data interlinking and can be done by adding a link to the equivalent entity using the `sameAs` attribute.
- Every entity has a type (i.e. Person, Place, Organization, …) and every type has its own set of properties. When we complete all the properties of an entity we increase the entity visibility and usefulness.  

When should I link one entity to another? 
_____________

By running the analysis on the property description text of an entity you can *link* it to other entities. WordLift will store these relationships between one entity and other entities in the `graph <key-concepts.html#knowledge-graph>`_ using the Dublin Core property ``dct:related``. This information will be used to suggest new connections between the contents of your site. Creating links among relevant entities will create more structure for your content, even though it is not mandatory to do so. You should always link entities that can help other users discover relevant contents (i.e. the entity *[Berners-Lee]* shall be linked to entity *[Web]* as the two concepts are strictly related.)

What are the languages supported by WordLift? 
_____________

WordLift currently supports the following languages: English, 中文 (Chinese), Español (Spanish), Русский (Russian), Português (Portuguese), Français (French), Deutsch (German), Italiano (Italian), Nederlands (Dutch), Svenska (Swedish) and Dansk (Danish). 

.. note::
	WordLift supports one language at the time. The main language of the website can be configured from the WordLift settings. 
	Review the `configuration settings <getting-started.html#configuration>`_ for more information. 

What are the datasets WordLift uses for named entity recognition? 
_____________

WordLift by default uses DBpedia and Freebase to detect and link named entities. With a custom configuration, the content analysis services provided by `Redlink <http://www.redlink.co>`_ and available via our professional services, can use any RDF-based `graph <key-concepts.html#knowledge-graph>`_. It is also possible to use *multiple graphs* for named entity recognition and `dereferencing <key-concepts.html#dereferencing-http-uris>`_. 

What is a triple? 
_____________

A triple is a set of three elements: a subject, a predicate, and an object. Triples are linked together to form a `graph <key-concepts.html#knowledge-graph>`_ that is without hierarchy, is machine readable, and can be used to infer new facts. Triples in WordLift describe facts as metadata about an article or an entity. 
