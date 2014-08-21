Key Concepts
===============

Entities
_____________

An **entity** is something that exists in the real-world: celebrities, cities, sports teams, buildings, geographical features, movies, celestial objects and works of art are all entities. For a long time, more than four decades, we teached computers to recognise things by simply matching keywords. Now computers, just like humans do, understand that a text like *[Thubten Gyatso]* is not just made of two words but, it has a much richer meaning. 

*[Thubten Gyatso]* is a person, more specifically he's the 13th Dalai Lama who was born in the Tsang-Ü province in Tibet on the 12th of February 1876. All this information - collectively shared in public sources like Wikipedia and Freebase - is organised in intelligent models known as **Graphs** that are helping computers thinking the way we do and helping us finding this information more quickly and even compute it (i.e. providing answers to question like *"Was Trinley Gyatso his predecessor?"*).   

Knowledge Graph
_____________



Vocabulary
_____________
A **vocabulary** is a collection of things (or entities in our case). In WordLift users can create their own custom vocabulary by creating entities and describing their properties (i.e. [Europe Day] is held on 9 May and celebrates peace and unity in Europe). These entities might already exists in publicly available sources like Wikipedia and Freebase. In this case WordLift provides a list of suggested entities that can be *linked* to (or reconciled with). When we link entities WordLift uses the ```owl:sameAs <http://www.w3.org/TR/owl-ref/#sameAs-def>`_`` property and this means that we're talking about the same *thing* (both entities share the same "identity");yes, I'm talking about that same [Europe Day] that Freebase describes at the URI http://www.freebase.com/m/04f6ymq. This linking process is also called reconciliation or disambiguation.   

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


