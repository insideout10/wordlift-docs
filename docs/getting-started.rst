Getting Started
===============

.. note::

    WordLift 3 is currently in active development, and is being tested by a restricted team of testers. If you'd like to
    join the team, subscribe on join.wordlift.it_.

.. warning::

    Even though we're already using WordLift 3 on some production web sites and there's no harm to data, we **strongly
    suggest** to make a full back-up of your site data before installing WordLift.


Compatibility
_____________

WordLift is currently being tested with WordPress_ 4.2.4 and later.


Installation
____________

Download the provided zip file to the `wp-content/plugins` directory of your WordPress_ installation. Unzip the file,
from the command line::

    unzip wordlift.zip

After installing WordLift you should see the logo on the top right corner of your dashboard menu. 

.. image:: /images/wordpress-admin-bar.png


Activation
__________

To activate the plugin you will need a `WordLift key <key-concepts.html#wordlift_key>`_. You might receive this key from us or from an automatic email system righ after subscribing to the service from the WordLift_ website (*coming up*). 

From the WordPress administration menu, click on *Plugins* / *Installed Plugins*. Then click on *Settings* on the
WordLift plugin.

Configuration
_____________

Hover on the WordLift logo on the upper right corner, a menu will open. Click on *Settings* to open the settings screen:

.. image:: /images/wordlift-settings-menu.png

From this screen you can set the following settings:

.. image:: /images/wordlift-settings-screen.png

New Entity Posts displayed as
    If *index* new Entity Posts by default are displayed as an index of posts referencing that entity.
    If *page* new Entity Posts by default are displayed as a page with the entity image and description.

Enable color coding of entities
    If enabled, entities in post content are highlighted on the front-end web.

Application Key
    A *unique key* which uniquely identifies your blog.

User ID
    Your user ID (numeric).

Dataset Name
    The name of the dataset associated with your blog.

Dataset URI
    The URL of the dataset *triple store* (**no trailing slash** at the end), e.g. http://data.redlink.io/000/dataset

Analysis Name
    The name of the analysis to use to analyze the blog contents.

Site Language
    The default language for the blog, used as a language code in the *triple store*.


Configure all the settings with the values that the WordLift team will provide to you. Don't forget to save the changes
by clicking on *Save Changes*.


.. note::

    If you have a Redlink_ account, you can use your own settings. Refer to my.redlink.io_ for more information.


You can now continue to the :doc:`key-concepts` page.


.. _join.wordlift.it: http://join.wordlift.it/
.. _my.redlink.io: http://my.redlink.io
.. _Redlink: http://redlink.co/
.. _WordPress: http://wordpress.org/
.. _WordLift: http://wordlift.it/
