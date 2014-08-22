Key Concepts
===============
Here is the terminology describing the core concepts that will help you set up and manage your contents with WordLift:

Entity
_____________
An **entity** is something that exists in the real-world: celebrities, cities, sports teams, buildings, geographical features, movies, celestial objects and works of art are all entities. For a long time, more than four decades, we teached computers to recognise things by simply matching keywords. 


Now computers, just like humans do, understand that a text like *[Thubten Gyatso]* is not just made of two words but, it has a much richer meaning. *[Thubten Gyatso]* is a person, more specifically he's the 13th Dalai Lama who was born in the Tsang-Ü province in Tibet on the 12th of February 1876. 


All this information - collectively shared in public sources like Wikipedia and Freebase - is organised in intelligent models known as **Graphs** that are helping computers thinking the way we do and helping us finding this information more quickly and even compute it (i.e. providing answers to question like *"Was Trinley Gyatso his predecessor?"*).   

Vocabulary
_____________
A **vocabulary** is a collection of things (or entities in our case). 

In WordLift users can create their own custom vocabulary by creating entities and describing their properties (i.e. *[Europe Day]* is held on 9 May and celebrates peace and unity in Europe). These entities might already exist in publicly available sources like Wikipedia and Freebase. In this case WordLift provides a list of suggested entities that can be *linked* to (or reconciled with). 


When we link entities WordLift uses the ``owl:sameAs`` property; this means that we're talking about the same *thing* (or simply that both entities share the same "identity"): "Yes, I'm talking about that same *[Europe Day]* that Freebase describes with machine id **m/04f6ymq**". 


This linking process is also called `reconciliation`_ or disambiguation.   

Knowledge Graph
_____________
A **knowledge graph** is a network of all kind of entities that are relevant to a specific domain or to an organization. 
They are not limited to abstract concepts and relations (as with a vocabulary) but also contain the instances of the things they describe.

Using WordLift as new entities are added in the vocabulary, properties for these entities are populated using the 
*ease-to-use* WordPress editing interfaces and new posts are enriched with these entities a knowledge graph is 
created and published as `RDF`_ graph in the cloud.

RDF
_____________
**RDF** stands for Resource Description Framework. 
RDF is a W3C standard language for representing information. 

Reconciliation
_____________
**Reconciling** entities we store in our own `vocabulary`_ with entities available elsewhere provides computers with an unambiguous way to identify the things we're talking about. 


*[Apple]* in a specific article might refer to a rather typical British psychedelic-pop group rather than to a World famous computer company or the forbidden fruit. This becomes important when third party applications like search engines need to provide valuable content for users searching for articles on *[Apple]* the psychedelic-pop band and not the other two *Apples*. 

`Reconciling`_ entities means providing computers with unambiguous identifications of the *entities* we talk about.  

Semantic Fingerprint
_____________
As result of the semantic annotation of portions of the text we write a *unique linked identifier* is added to the HTML code. This identifier is known as **semantic fingerprint**. 


Annotating contents, also known as *semantic enrichment* or *lifting*, creates metadata that computers can understand. 
Just like in forensic science human fingerprints are used to identify humans appearing on a crime scene, in computer science we use semantic fingerprints to tell computers what `entities <https://wordlift.readthedocs.org/en/latest/key-concepts.html#entity>`_ we're referring to. 


WordLift re-uses these semantic fingerprints for adding Schema.org markup and for re-purposing contents using `Widgets <https://wordlift.readthedocs.org/en/latest/key-concepts.html#widget>`_.    


Widget
_____________
A **widget** in WordLift is a dynamic visualisation that can be added by the editors to a page via `Shortcode <http://codex.wordpress.org/Shortcode>`_ or using the WordLift menu. 

A Widget is executed by the end-user's browser when accessing a page. 
A Widget typically displays informations being stored in the `knowledge graph`_ and creates dynamic connections between different contents.  

.. note::

    This documentation is still under construction. 


