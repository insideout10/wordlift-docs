How To Import and Export the User Vocabulary 
========

There are several cases where a user decides to export or import the vocabulary of terms created with WordLift. Let’s see them in details: 

1. The site needs to be migrated from one server to another,
2. The content structure of a website created for a language can be replicated for another language. In this case the website is not using a multilingual plugin such as WPML as contents might be different in the different languages. When using plugins such as WPML posts and pages hold the contents in multiple language - this works very well when all the same contents are translated 1:1 in the different languages. This approach is less effective when the site needs to have a different structure for each language,
3. The `vocabulary <key-concepts.html#vocabulary>`_ on one site can be re-used for tagging another website running a separate WordLift key 

WordPress natively provides an Export/Import functionality that assist the editor in both of these scenarios. This functionality has been enhanced for any WordLift’s user to ensure entities can be moved back and forth across multiple websites. 

How to Export the WordLift Vocabulary
_____________

To export the vocabulary from the *origin website* go in the WordPress menù under Tools and click the Export link. Choose to export the vocabulary only (unless you need to export the entire website). 

How to Import the WordLift Vocabulary
_____________

To import the vocabulary in the *destination website* go in the WordPress menù under Tools and click the Import link. Choose the XML file that was produced with the Export function and remember to choose *Import WordPress* and to check the option *Download and import file attachments* to get all entities imported.

.. note::

	When data is imported from a website in one language (let's say English) - the data is saved using the language being set under the WordLift's configuration tab of the destination website.      

.. warning::

	For the images there is currently a limitation in WordPress that might prevent the right images to be imported. More information are available on the `wptips website <http://wptips.me/how-to-import-images-when-importing-posts-from-a-wordpress-export-file/>`_

Connecting source and destination websites with the sameAs links
_____________

When importing the vocabulary on a website with a different URL (this would be case 2 or 3) WordLift automatically populates the sameAs links with the equivalent entity from the source site. 

Entity interlinking and why is so important
--------------

This process is called entity interlinking and it is beneficial for the metadata being published as provides further means of reuse.

Let’s say a developer is writing an application to display events and that these events are created with WordLift in two different website (one website for English and the other one for German) - the application will be able to use the sameAs links to retrive the content in the required language: English if let’s say the users are in the UK and German if the users are from Germany. The otherwise separate datasets will be effectively combined.    

.. note::

	When importing the vocabulary on a website with the same URL (this would be case 1) the sameAs links are not added by the importer. 

Vocabulary sharing and how to keep it in sync
_____________

.. warning::

	When sharing the same vocabulary on multiple websites the risk of duplicating the content is high and, as a general rule, this shall be prevented. 

When the vocabulary grows on one site and we need to re-use it on another site the import/export might not be the best approach and a different solution can be used. 

Sharing terms among different websites 
--------------

WordLift - wth the enterprise license - allows the user to configure the NLP with multiple datasets in order to perform the content analysis on the articles. An enterprise - for instance - could chose to have let’s say a product website that uses, besides the terms created within its internal vocabulary, all the terms created in the vocabulary of the corporate website. This way when an entity is created on the corporate website for describing a new team member, this entity will be made immediately available for tagging content on the product website that have to do with this new person. 

Moreover WordLift will automatically perform the entity interlinking without asking the editor any further action (the entity on the product website will have the sameAs links pointing to the entity’s URL on the corporate website). In this way all the terms created on one site can be used for annotating content on other websites. When constructing the product website the developer might also chose to redirect the traffic to the entity pages on the source site by using the sameAs links (this will avoid content duplication and will increase the interlinking between the different websites).
    

       
