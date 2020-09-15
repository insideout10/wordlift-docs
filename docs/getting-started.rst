Getting Started
===============

.. note::

    We **suggest** our users to make a full back-up of their website data before installing WordLift.

===============
Overview
===============

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube-nocookie.com/embed/AR2pBOTLsy4" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


**WordLift** brings the power of *Artificial Intelligence* to web publishers around the World.

**WordLift** is a plugin for WordPress designed to help you create, structure and visualize your content and to publish it as `Linked Open Data <key-concepts.html#linked-open-data>`_ following **Tim Berners-Lee**'s `Linked Data Principles <http://www.w3.org/DesignIssues/LinkedData.html>`_.

Linked Data is the language machines can read and understand in order to seamlessly analyze content, index it and fetch answers back to users. 
Linked Data technologies allow software agents and search crawlers find, share and integrate information across different resources.

**WordLift** supports bloggers and site owners building *beautifully structured web sites* and reach their maximum potential audiences:

- It understands the text you write and structures it to allow you to create effective navigation flows and make sure commercial search engines like Google, Bing, Yandex and Yahoo! receive the structured data they need to properly index and rank your content.

- It  enriches your blog posts and pages with facts, links and images, and organizes them in relationship to each other, to internal vocabularies, and to other openly available data sources like DBpedia and Wikidata, increasing your readers’ engagement.

.. note::
        **WordLift** is available to all for a monthly fee. Find out more and get your activation key directly `on our website <https://wordlift.io>`_.

===============
Features at a glance
===============

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/TzsIz-mjY94" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

**WordLift** is a **semantic editor** for WordPress to help writing, organizing, tagging and sharing content online. 
**WordLift** is designed for bloggers, journalists and content creators to inspire and make writing more productive.

**WordLift** adds `semantic annotation <key-concepts.html#semantic-fingerprint>`_ and combines information publicly available as `linked open data <key-concepts.html#linked-open-data>`_ to support the editorial workflow by suggesting relevant information, images and links.

WordLift brings to content editors
_____________

* support for **self-organising** (or structuring) **content** using publicly (or privately) available `knowledge graphs <key-concepts.html#knowledge-graph>`_ (`linked open data <key-concepts.html#linked-open-data>`_)
* an easy way to **build your own dataset** made of *web content*, *semantic annotations* and a *custom vocabulary* 
* support for creating web content using **contextually relevant fact-based information**
* valued and **free to use photos and illustrations** from the Commons community ranging from maps to astronomical imagery to photographs, artworks and more
* insightful **visualisations to engage the reader**
* new means to drive business growth with **meaningful content discovery paths**
* content tagging for **better SEO**

Websites built with WordLift bring to readers
_____________

* multiple means of searching and accessing **editorial content around a specific topic** 
* **contextual information** helping readers with limited domain understanding
* an **intuitive overview of all content being written** *on the site* and *around a specific topic* or graph of topics
* meaningful **content recommendations** 

===============
Installation
===============

.. note::

    We **suggest** our users to make a full back-up of their website data before installing WordLift.


Requirements
____________

WordLift is currently available on WordPress_ 4.4 and later.


Installation
____________

You can install **WordLift** from the `WordPress plugin directory <https://wordpress.org/plugins/wordlift/>`_ or manually by uploading the files to your server.


Automatic Installation
-----------------
Automatic installation is the easiest way to install WordLift. WordPress handles the file transfers itself and you don’t need to leave your web browser. To do an automatic install of WordLift, log in to your WordPress dashboard, navigate to the Plugins menu and click Add New.

In the search field type “WordLift” and click Search Plugins. Once you’ve found our plugin you can view details about it such as the description, the features, and user reviews. Most importantly of course, you can install it by simply clicking “Install Now”.


Manual Installation
-----------------
The manual installation method involves *downloading our plugin* and *uploading it to your webserver* using your favourite FTP application. 

Download the provided zip file to the `wp-content/plugins` directory of your WordPress_ installation. Unzip the file,

from the command line::

    unzip wordlift.zip

More information on the manual installation are available on the `WordPress Codex <http://codex.wordpress.org/Managing_Plugins#Manual_Plugin_Installation>`_ website.   

Activation
__________

To activate the plugin you need a `WordLift key <key-concepts.html#wordlift-key>`_. You receive this key after `purchasing a subscription plan <https://wordlift.io/pricing/>`_ the WordLift_ website. An automatic email will be then sent to you containing your key and account information. 

You can use the setup Wizard upon startup to activate your subscription. 

.. image:: /images/wordlift-setup-wizard.gif

When doing so you are able to configure the `key <key-concepts.html#wordlift-key>`_, the entity base path (the URL pattern of the WordLift internal vocabulary), the languange used on the website and the publisher of the website. 

Alternatively, from the WordPress administration menu, click on *Plugins* / *Installed Plugins*. Then click on *Settings* on the
WordLift plugin.


Configuration
_____________

The *Settings* are also accessible by hovering on the WordLift logo on the WordPress dashboard menu; from there a menu will open. 
Click on *Settings* to open the settings screen:

.. image:: /images/wordlift-settings-screen.png

From *Settings* screen, as from the Wizard, you can configure:

WordLift Key
    The `WordLift Key <key-concepts.html#wordlift-key>`_, required to activate the plug-in that can be purchased from the `website <https://wordlift.io/pricing/>`_.
    
Entity Base Path
    When selecting or creating new entities with WordLift, you are actively building your internal vocabulary, adding pages to  your website. When you first built your website, you chose a pattern for the url of the pages you were going to add, such as www.domain.com/name-of-the-page or www.domain.com/seo-keyword/name-of-the-page. 
    The same applies with all the pages created with WordLift inside your vocabulary.
    By default WordLift will add the word “vocabulary” between your root domain and the name of the page: www.domain.com/vocabulary/name-of-the-entity-page.
    You can delete the word vocabulary if you want the new entity page to be inside your root domain folder: www.domain.com/name-of-the-entity-page.
    Or you can replace vocabulary with another keyword (or keywords) of your choice, for SEO or branding reason: www.domain.com/seo-keyword/name-of-the-entity-page.

Site Language
    The main language used on your website. This is the language that will be used by WordLift when creating the editorial metadata of your content. Be aware, each key should be used for one language only.

Publisher
    The person or the organization publishing the content of the website. This is also an entity that can be created directly from this setting screen. This information is used to enrich the metadata on your website.  

.. note::
        For more information on the multilingual support of WordLift `read here <faq.html#what-are-the-languages-supported-by-wordlift>`_.


You can now continue to the :doc:`key-concepts` page or head directly to the :doc:`analysis` page.


.. _join.wordlift.it: https://join.wordlift.it/
.. _my.redlink.io: https://my.redlink.io
.. _Redlink: https://redlink.co/
.. _WordPress: https://wordpress.org/
.. _WordLift: https://wordlift.io/

