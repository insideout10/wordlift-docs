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

To activate the plugin you will need a `WordLift key <key-concepts.html#wordlift-key>`_. You might receive this key from us or from an automatic email system righ after subscribing to the service from the WordLift_ website (*coming up*). 

From the WordPress administration menu, click on *Plugins* / *Installed Plugins*. Then click on *Settings* on the
WordLift plugin.

Configuration
_____________

The *Settings* are also accessible by hovering on the WordLift logo on the upper right corner; from there a menu will open. 
Click on *Settings* to open the settings screen:

.. image:: /images/wordlift-settings-menu.png

.. image:: /images/wordlift-settings-screen.png

From *Settings* screen you can configure:

WordLift Key
    Your `WordLift Key <key-concepts.html#wordlift-key>`_, 

Enable color coding on front-end
    The option for enabling/disabling the color highlighting of `entities <key-concepts.html#entity>`_ in post contents. 

Site Language
    The main language used on your website. 

    :: note
        For more information on the multilingual support of WordLift `read here <faq.html#what-are-the-languages-supported-by-wordlift>`_

If you have a Redlink_ account, you can use your own application settings by enabling the *Advanced Settings* of WordLift. This is done by adding the following line to your `wp-config.php` ::

    define('WL_ENABLE_ADVANCED_CONFIGURATION', true);

In this case the following options can be configured: 

.. image:: /images/wordlift-settings-advanced-menu.png

API URL
    The Redlink URL base (*http://data.redlink.io/91/be2* in this case).

Redlink Key
    The *Redlink key* associated to your account.

Redlink Dataset name
    The name of the dataset associated with your blog.

Redlink Dataset URI
    The URL of the dataset *triple store* (**no trailing slash** at the end), e.g. http://data.redlink.io/000/dataset

Redlink Dataset Name
    The name of the application configured in your Redlink account.

.. note::

    Please refer to the Redlink_ team if you would like to use WordLift in conjunction to your Redlink account.

Configure all the settings with the values that the WordLift team will provide to you. Don't forget to save the changes
by clicking on *Save Changes*.


You can now continue to the :doc:`key-concepts` page.


.. _join.wordlift.it: http://join.wordlift.it/
.. _my.redlink.io: http://my.redlink.io
.. _Redlink: http://redlink.co/
.. _WordPress: http://wordpress.org/
.. _WordLift: http://wordlift.it/
