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

WordLift **loads automatically the latest version of the schema.org vocabulary**, supports **all the available schema types**, and allows you to personalize your content model easily while taking care of the injection of the json-ld on your pages.

Advanced Schema types
_____________

HowTo
^^^^^^^^^^^^^^^
HowTo Schema allows you to explain exact instructions to achieving a wanted result by performing a sequence of steps. This can range from guides explaining "How to start your own business" or simple DIY recipes.

Recipe
^^^^^^^^^^^^^^^
A recipe schema allows you to specify steps in your recipe, varying from nutritional information to the method of cooking. This can all be done by choosing specific keywords under the properties. Learn `how to add schema markup for recipes <https://wordlift.io/academy-entries/schema-markup-for-recipe/>`_.

Course
^^^^^^^^^^^^^^^
Course schema markup is the specific entity type for web pages that describe an educational course that may be offered online or in person by public and private schools, colleges, and universities. Learn `how to add course schema markup to your content <https://wordlift.io/academy-entries/course-schema-markup/>`_.

FAQ
^^^^^^^^^^^^^^^
FAQ stands for "Frequently Asked Questions", where the questions that most people ask you about your activities can be listed on this webpage. Some properties include breadcrumbs and lastreviewed, which is the date on which the content on this web page was last reviewed for accuracy and/or completeness.
Learn more on `how to use the FAQPage Schema type <https://wordlift.io/academy-entries/how-to-use-faq-schema-type/>`_.

Review
^^^^^^^^^^^^^^^
Review schema shows you the opinions and feedback regarding an item, a movie or a service.

Product
^^^^^^^^^^^^^^^
Product markup communicates to Google a series of essential data for your customers such as product description, image, price, availability, conditions, and user ratings.
With WordLift you can create a `product knowledge graph <https://wordlift.io/blog/en/product-knowledge-graph/>`_ and help Google discover more about the brand, the color, the condition (new, used, reconditioned etc) the shipping details and a lot more.
If you are using WooCommerce here is `all you need to know about the product schema <https://wordlift.io/blog/en/schema-markup-woocommerce/>`_.

Event
^^^^^^^^^^^^^^^
Event schema is a type of structured data markup that informs search engines that a particular web page is an event that takes place offline or online, such as concerts, seminars/webinars, meetings and more. Learn `how to add event schema markup to your website <https://wordlift.io/academy-entries/event-schema-markup/>`_.

Service
^^^^^^^^^^^^^^^
Service schema helps search engines understand your business and your services.
Learn more on `how to use the service markup <https://wordlift.io/academy-entries/service-markup/>`_.

LocalBusiness
^^^^^^^^^^^^^^^
LocalBusiness is the schema markup for a particular physical business or branch of an organization, such as for example a restaurant, a particular branch of a restaurant chain, a branch of a bank, a medical practice, a club, a bowling alley, etc. Learn `how to add LocalBusiness schema to your web pages <https://wordlift.io/academy-entries/how-to-add-localbusiness-schema/>`_.

Advanced Custom Fields
_____________

To follow a step-by-step tutorial head on to our blogpost where our specialist shows you `how to enhance your content model using Wordlift mappings. <https://wordlift.io/academy-entries/wordlift-mappings-tutorial/>`_

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
