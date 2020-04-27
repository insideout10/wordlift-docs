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

WordLift loads automatically the latest version of schema.org and allows you to personalize your content model easily while taking care of the injection of the json-ld on your pages. 

Getting Started
_____________

Requirements
^^^^^^^^^^^^^^^

* `Advanced Custom Fields <https://wordpress.org/plugins/advanced-custom-fields/>`_ (ACF)

.. image::

* Advanced Custom Fields for schema.org by WordLift (`Contact our SEO team to get started <https://wordlift.io/customize-your-plan/>`_) 

Add Custom Fields
^^^^^^^^^^^^^^^
First create a **new custom field** by clicking on **Field Group** and choosing a title.

.. image::
.. image::

Then add your first **field**

.. image::

* **Field Label** is what the user will see editing a post
* **Field Name** from schema.org (e.g. endDate)
* **Field Type** “Date time picker” in the case of endDate

.. image::

* **Instructions** for authors. Shown when submitting data
* **Required?** whether this field is needed or not in order to publish a post

.. image::

* **Default Value**, you can fill this box if you want a default data when creating a post
* **Placeholder Text**, appears within the input
* **Prepend**, appears before the input
* **Append**, appears after the input
* **Character Limit**
* **Conditional Logic**
* **Wrapper Attributes**

.. image::

* **Location**
		**Rules**, here you can choose to use this ACF if for example your Post Type is equal or not equal to one of your Post Types


.. image::

This is how it looks for authors while creating or editing a post:

.. image::

Add New mapping
^^^^^^^^^^^^^^^

First go on **Schema.org Types** and **Sync Schema.org classes**

.. image::
.. image::

Then go on **Mappings** and add a new one.
Choose a **title** and at least one **Rule**

.. image::

Add at least one **Property**:

* **Property name** 
* **Field Type**, select ACF to use Custom Fields
* **Field Text**, choose which *custom field* to use for that property
* **Transform Function**