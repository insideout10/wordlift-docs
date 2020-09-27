Mappings
========

Mappings are designed to help us organize and structure content while improving the SEO on our website. 

**The markup in schema.org adds meaning to your content** for search engines but the real benefits come when you **use structured data as the basis for your content model.**

We call it the **entity-based content model** and you can learn more about by watching the following webinars:

* `Content Modeling for Search Optimization with Cruce Saunders <https://wordlift.io/academy-entries/content-modeling/>`_
* `Get Started with Structured Content and Schema.org <https://wordlift.io/academy-entries/structure-your-content/>`_

Or by `booking a call with our SEO experts. <https://wordlift.io/book-a-demo>`_.

WordLift mappings have been developed as an integration for the `Advanced Custom Fields <https://www.advancedcustomfields.com/>`_ plugin and allows you to either: 
 
* re-use fields that you might have already configured with ACF on your CMS or,
* create new fields based on the schema.org taxonomy

Supported Schema types 
_____________

WordLift loads automatically the latest version of schema.org and allows you to personalize your content model easily while taking care of the injection of the json-ld on your pages. 

Advanced Schema types
_____________

HowTo
^^^^^^^^^^^^^^^
HowTo Schema allows you to explain exact instructions to achieving a wanted result by performing a sequence of steps. This can range from guides explaining "How to start your own business" or simple DIY recipes.

Recipe
^^^^^^^^^^^^^^^
A recipe schema allows you to specify steps in your recipe, varying from nutritional information to the method of cooking. This can all be done by choosing specific keywords under the properties. 

FAQ
^^^^^^^^^^^^^^^
FAQ stands for "Frequently Asked Questions", where the questions that most people ask you about your activities can be listed on this webpage. Some properties include breadcrumbs and lastreviewed, which is the date on which the content on this web page was last reviewed for accuracy and/or completeness.

Review
^^^^^^^^^^^^^^^
Review schema shows you the opinions and feedback regarding an item, a movie or a service.

Advanced Custom Fields
_____________

To follow a step-by-step tutorial head on to our blogpost where our specialist explains `how to enhance your content model using Wordlift mappings. <https://wordlift.io/academy-entries/wordlift-mappings-tutorial/>`_

Requirements
^^^^^^^^^^^^^^^

* `Advanced Custom Fields <https://wordpress.org/plugins/advanced-custom-fields/>`_ (ACF)

.. image:: /images/mappings-acf.png

* Advanced Custom Fields for schema.org by WordLift (`Contact our SEO team to get started <https://wordlift.io/customize-your-plan/>`_) 

Add Custom Fields
^^^^^^^^^^^^^^^
First create a **new custom field** by clicking on **Field Group** and choosing a title.

.. image:: /images/mapping-custom-fields.png
.. image:: /images/mappings-field-group.png

Then add your first **field**

.. image:: /images/mappings-field-step-1.png

* **Field Label** is what the user will see editing a post
* **Field Name** from schema.org (e.g. endDate)
* **Field Type** “Date time picker” in the case of endDate

.. image:: /images/mappings-field-type.png

* **Instructions** for authors. Shown when submitting data
* **Required?** whether this field is needed or not in order to publish a post

.. image:: /images/mappings-field-example-1.png

* **Default Value**, you can fill this box if you want a default data when creating a post
* **Placeholder Text**, appears within the input
* **Prepend**, appears before the input
* **Append**, appears after the input
* **Character Limit**
* **Conditional Logic**
* **Wrapper Attributes**

.. image:: /images/mappings-field-example-2.png

* **Location**
		**Rules**, here you can choose to use this ACF if for example your Post Type is equal or not equal to one of your Post Types


.. image:: /images/mappings-rules.png

This is how it looks for authors while creating or editing a post:

.. image:: /images/mappings-draft-example.png


Add New mapping
^^^^^^^^^^^^^^^

First go on **Schema.org Types** and **Sync Schema.org classes**

.. image:: /images/mappings-schema.png
.. image:: /images/mappings-sync-schema.png

Then go on **Mappings** and add a new one.

.. image:: /images/mappings-step-1.png

Choose a **title** and at least one **Rule**

.. image:: /images/mappings-step-2.png

Add at least one **Property**:

.. image:: /images/mappings-step-5.png

* **Property name**, give a name to your property
* **Field Type**, select ACF to use Custom Fields
* **Field Text**, choose which *custom field* to use for that property
* **Transform Function**
