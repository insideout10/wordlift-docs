Key Concepts
===============
Here is the terminology describing the core concepts that will help you set up and manage your contents with WordLift:

Entities
_____________
An **entity** is something that exists in the real-world: celebrities, cities, sports teams, buildings, geographical features, movies, celestial objects and works of art are all entities. For a long time, more than four decades, we teached computers to recognise things by simply matching keywords. 


Now computers, just like humans do, understand that a text like *[Thubten Gyatso]* is not just made of two words but, it has a much richer meaning. *[Thubten Gyatso]* is a person, more specifically he's the 13th Dalai Lama who was born in the Tsang-Ü province in Tibet on the 12th of February 1876. 


All this information - collectively shared in public sources like Wikipedia and Freebase - is organised in intelligent models known as **Graphs** that are helping computers thinking the way we do and helping us finding this information more quickly and even compute it (i.e. providing answers to question like *"Was Trinley Gyatso his predecessor?"*).   

Vocabulary
_____________
A **vocabulary** is a collection of things (or entities in our case). In WordLift users can create their own custom vocabulary by creating entities and describing their properties (i.e. *[Europe Day]* is held on 9 May and celebrates peace and unity in Europe). These entities might already exist in publicly available sources like Wikipedia and Freebase. In this case WordLift provides a list of suggested entities that can be *linked* to (or reconciled with). 


When we link entities WordLift uses the ``owl:sameAs`` property; this means that we're talking about the same *thing* (or simply that both entities share the same "identity"): "Yes, I'm talking about that same *[Europe Day]* that Freebase describes with machine id `m/04f6ymq <http://www.freebase.com/m/04f6ymq>`_". 


This linking process is also called reconciliation or disambiguation.   

Knowledge Graph
_____________
A **knowledge graph** is a network of all kind of entities that are relevant to a specific domain or to an organization. 
They are not limited to abstract concepts and relations (as with a vocabulary) but also contain the instances of the things they describe.

Using WordLift as new entities are added in the vocabulary, properties for these entities are populated using the 
*ease-to-use* WordPress editing interfaces and new posts are enriched with these entities a knowledge graph is 
created and published as RDF graph the cloud.

RDF
_____________
RDF stands for Resource Description Framework and is a W3C standard language for representing information. 

Reconciliation
_____________
Reconciling entities we store in our own vocabulary with entities available elsewhere provides computers with an unambiguous way to identify the things we're talking about. [Apple] in a specific article might refer to a rather typical British psychedelic-pop group rather than to a World famous computer company or to the forbidden fruit. This becomes important when third party applications like search engine need to provide valuable content for users searching for [Apple] the psychedelic-pop band and not the other two. As we reconciled entities we're providing unambiguous descriptions of the *things* with describe in our contents.  

Semantic Fingerprint
_____________
It is the process of annotating resources like portions of the text we write (i.e. [Europe Day] or [Thubten Gyatso]) or fragments of the media we add in our pages with unique linked indentifiers. Annotating contents, also known as semantic enrichment, creates metadata that computers can understand. WordLift re-uses the semantic fingerprints editors create for adding Schema.org markup and re-purposing contents using Widgets.    


Widget
_____________

.. note::

    This documentation is still under construction. 


