Export & Import of the Vocabulary
========

There are several cases where a user decides to export or import the vocabulary of terms created with **WordLift**. Let’s see them in details: 

1. The site needs to be migrated from one server to another,
2. The content structure of a website created for a language can be replicated for another language (and the website is not using a multilingual plugin such as `WPML <https://wpml.org/>`_), 
3. The `vocabulary <key-concepts.html#vocabulary>`_ on one site can be re-used for tagging another website running a separate **WordLift** key. 

WordPress natively provides both `Export <https://codex.wordpress.org/Tools_Export_Screen>`_ and `Import <https://codex.wordpress.org/Tools_Import_Screen>`_ functionalities. This functionalities have been enhanced for any **WordLift**’s user to ensure that also entities can be moved back and forth across multiple websites. 

How to Export the **WordLift** Vocabulary
_____________

To export the vocabulary from the *origin website* go in the WordPress menù under Tools and click the Export link. Choose to export the vocabulary only (unless you need to export the entire website). 

How to Import the **WordLift** Vocabulary
_____________

To import the vocabulary in the *destination website* go in the WordPress menù under Tools and click the Import link. Choose the XML file that was produced with the Export function and remember to choose *Import WordPress* and to check the option *Download and import file attachments* to get all entities imported.

.. note::

	When data is imported from a website in one language (let's say English) - the data is saved using the language being set under the **WordLift**'s configuration tab of the destination website.      

.. warning::

	For the images there is currently a limitation in WordPress that might prevent the right images to be imported. More information are available on the `wptips website <http://wptips.me/how-to-import-images-when-importing-posts-from-a-wordpress-export-file/>`_.

Connecting source and destination websites with *sameAs* links
_____________

When importing the vocabulary on a website with a different URL (this would be case 2 or 3 from the scenarios listed above) **WordLift** automatically populates all *sameAs* links with the equivalent entity on the *origin website*. 

Entity interlinking and why is so important
--------------

This process is called *entity interlinking* (or `entity reconciliation <key-concepts.html#reconciliation>`_) and it is beneficial for the metadata being published as it provides further means of data reuse.

Let’s say a developer is writing an application to display events and that these events are created with **WordLift** in two different website (one website for English and the other one for German) - the application will be able to use the *sameAs* links to retrive the content in the required language: English if let’s say the users are in the UK and German if the users are from Germany. The otherwise separate datasets will be effectively combined.    

.. note::

	When importing the vocabulary on a website with the same URL (this would be case 1) the *sameAs* links are not added by the importer. 

Vocabulary sharing and how to keep it in sync
_____________

.. warning::

	When sharing the same vocabulary on multiple websites the risk of duplicating the content is high and, as a general rule, this shall be prevented. 

When the vocabulary grows on one site and we need to re-use it in another site the Export & Import functions might not be the best approach and a different solution can be used (see below).  

Sharing terms among different websites 
--------------

**WordLift** allows the user to configure the NLP so that it will use multiple datasets for *content analysis* and `entity reconciliation <key-concepts.html#reconciliation>`_. An enterprise, for instance, could chose to have a product website that uses, besides the terms created within its internal vocabulary, all the terms created in the vocabulary of the corporate website. This way when an entity is created on the corporate website for describing a new team member, this entity is immediately made available on the product website. 

Moreover **WordLift** automatically performs the `entity reconciliation <key-concepts.html#reconciliation>`_ without asking the editor any further action (the entity on the product website will have the *sameAs* links pointing to the entity’s URL on the corporate website). In this way all the terms created on one site can be used for annotating content on another websites. When constructing the product website the developer might also chose to redirect the traffic to the entity pages on the source site by using the *sameAs* links (this will avoid content duplication and will increase the interlinking between the different websites).
       
