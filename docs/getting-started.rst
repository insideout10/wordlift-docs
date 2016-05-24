Getting Started
===============

.. warning::

    Even though we've been using WordLift v. 3 on production web sites for quite some times and there's no harm to data, we **strongly
    suggest** to make a full back-up of your site data before installing WordLift.


Compatibility
_____________

WordLift is currently available on WordPress_ 4.2 and later.


Installation
____________

You can install **WordPress** from the `WordPress plugin directory <https://wordpress.org/plugins/wordlift/>`_ or manually by uploading the files to your server.

=================
Automatic Installation
=================
Automatic installation is the easiest way to install WordLift. WordPress handles the file transfers itself and you don’t need to leave your web browser. To do an automatic install of WordLift, log in to your WordPress dashboard, navigate to the Plugins menu and click Add New.

In the search field type “WordLift” and click Search Plugins. Once you’ve found our plugin you can view details about it such as the point release, rating and description. Most importantly of course, you can install it by simply clicking “Install Now”.

=================
Manual Installation
=================
The manual installation method involves *downloading our plugin* and *uploading it to your webserver* using your favourite FTP application. 

Download the provided zip file to the `wp-content/plugins` directory of your WordPress_ installation. Unzip the file,

from the command line::


    unzip wordlift.zip

More information on the manual installation are available on the `WordPress Codex <http://codex.wordpress.org/Managing_Plugins#Manual_Plugin_Installation>`_ website.   

Activation
__________

To activate the plugin you need a `WordLift key <key-concepts.html#wordlift-key>`_. You receive this key after `purchasing a subscription plan <https://wordlift.io/#plan-and-price>`_ the WordLift_ website. An automatic email is sent containing your key and account information. 

From the WordPress administration menu, click on *Plugins* / *Installed Plugins*. Then click on *Settings* on the
WordLift plugin.


Configuration
_____________

The *Settings* are also accessible by hovering on the WordLift logo on the upper right corner; from there a menu will open. 
Click on *Settings* to open the settings screen:

.. image:: /images/wordlift-settings-screen.png

From *Settings* screen you can configure:

WordLift Key
    Your `WordLift Key <key-concepts.html#wordlift-key>`_, 

Site Language
    The main language used on your website. This is the language that will be used by WordLift when creating the editorial metadata of your content.  

.. note::
        For more information on the multilingual support of WordLift `read here <faq.html#what-are-the-languages-supported-by-wordlift>`_.

If you have a Redlink_ account, you can use your own application settings by enabling the *Advanced Settings* of WordLift. This is done by adding the following line to your `wp-config.php` ::

    define('WL_ENABLE_ADVANCED_CONFIGURATION', true);

In this case the following options can be configured: 

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

    Please refer to the Redlink_ team if you would like to use WordLift in conjunction with your Redlink account.

Configure all the settings with the values that the WordLift team will provide to you. Don't forget to save the changes
by clicking on *Save Changes*.


You can now continue to the :doc:`key-concepts` page or head directly to the :doc:`analysis` page.


.. _join.wordlift.it: http://join.wordlift.it/
.. _my.redlink.io: http://my.redlink.io
.. _Redlink: http://redlink.co/
.. _WordPress: http://wordpress.org/
.. _WordLift: http://wordlift.io/
