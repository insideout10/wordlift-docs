
Shortcodes
==========

WordLift provides several useful shortcodes to provide enhanced visualizations on your web site.

.. 
    Entity Shortcodes
    _________________


    Load entity data::

        [wl_entity_view uri=... suffix=...][/wl_entity_view]

    The URI of the entity is determined by combining the *uri* defined in the shortcode and the current address path.

    uri
        The *base* URI for remote resources (e.g. http://data.redlink.io/353/salzburgerland/)

    suffix
        *(optional)* The suffix for remote requests (e.g. '.json')


    Display the value of a property::

        [wl_entity_property name=... language=...]

    It must be used inside a *wl_entity_view*.

    name
        The full property name (e.g. http://www.w3.org/2000/01/rdf-schema#label)

    language
        *(optional)* The language (e.g. 'en'). If it's not specified, the shortcode looks for a value without a language.


    Display an image (using the *img* tag)::

        [wl_entity_image name=...]

    It must be used inside a *wl_entity_view*.

    name
        The full property name (e.g. http://schema.org/image)


    Display a date::

        [wl_entity_date name=... format=...]

    name
        The full property name (e.g. http://www.w3.org/2002/12/cal#dtstart)

    format
        *(optional, default 'Y m d')* The format to apply to the date (follows the PHP convention, see `PHP date`_ for more information).


    Display a duration::

        [wl_entity_duration name=... format=...]

    name
        The full property name (e.g. http://www.w3.org/2002/12/cal#dtstart)

    format
        *(optional, default '%d day(s), %h hour(s)')* The format to apply to the duration (follows the PHP convention, see `PHP DateInterval format`_ for more information).


    Example::

        [wl_entity_view uri="http://data.redlink.io/353/salzburgerland/"]</p>
            [wl_entity_property name="http://www.w3.org/2000/01/rdf-schema#label" language="en" /]
            [wl_entity_property name="http://linkedevents.org/ontology/atPlace&gt;http://www.w3.org/2000/01/rdf-schema#label" language="en" /]
            [wl_entity_property name="http://linkedevents.org/ontology/atPlace&gt;http://www.geonames.org/ontology#parentFeature&gt;http://www.w3.org/2000/01/rdf-schema#label" language="en" /]
            [wl_entity_date name="http://www.w3.org/2002/12/cal#dtstart" format="d/m/Y H:i" /]
            [wl_entity_date name="http://www.w3.org/2002/12/cal#dtend" format="d/m/Y" /]
            [wl_entity_duration name="http://schema.org/duration" /]
            [wl_entity_property name="http://www.w3.org/2002/12/cal#location" language="en" /]
            [wl_entity_property name="http://www.w3.org/2000/01/rdf-schema#comment" language="en"]
            [wl_entity_image name="http://schema.org/image" /]
        [/wl_entity_view]


Widget Shortcodes
_________________

WordLift widgets can be inserted in a post or page to give a rich visual presentation of the entities populating the blog. As the blog grows and entities are created and mentioned, the widgets update their content without intervention from the editor.

Chord widget::

    [wl_chord width=... height=... main_color=... depth=... global=...]
    
.. image:: /images/wordlift-shortcodes-chord.png
The Chord widget visualizes relations between entities, starting from the current post and the entities mentioned in it.

width
    *(optional)* Width of the chord. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the chord. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

main_color
    *(optional)* The chord's *base* color.

depth
    *(optional)* Maximum distance to travel in the entity graph in order to populate the chord. A small number limits the exploration of the main entity.

global
    *(optional)* When *global=true* the main entity of the chord is not the current post, but the most mentioned entity in the latest posts.
    
Timeline widget::
    
    [wl_timeline width=... height=... global=...]
    
.. image:: /images/wordlift-shortcodes-timeline.png
The Timeline widget displays a navigable list of chronologically ordered Event entities. The window on top shows details of the selected Events.

width
    *(optional)* Width of the timeline. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the timeline. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

global
    *(optional)* By default the timeline displays events (or events related to places) mentioned in the current post. When *global=true* the timeline displays events mentioned in the latest posts.

display_images_as
    *(optional)* When *display_images_as='background'* the timeline displays for each event the featured image of the entity as background.

excerpt_length
    *(optional)* Allows you to set the number of words that appear in the the excerpts of the timeline. 

.. note::
        When you create a timeline with WordLift you can pass in the shortcode optional parameters to set a variety of presentation options. These are derived from the TimelineJS library `read more here <https://timeline.knightlab.com/docs/options.html>`_.

Geomap widget::

    [wl_geomap width=... height=... global=...]
    
.. image:: /images/wordlift-shortcodes-geomap.png    
The Geomap widget displays "Place" entities on a map. Each Place has its own marker with a popup containing a thumbnail and links of the place.
    
width
    *(optional)* Width of the geomap. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the geomap. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

global
    *(optional)* By default the geomap displays places mentioned in the current post. When *global=true* the geomap displays all places mentioned in the blog.

Navigator widget::

    [wl_navigator]

The Navigator widget offers links to semantic-related posts in the blog. The search is made by considering the entities mentioned in the current post (in the order WHO, WHAT, WHERE, WHEN) and finding other blog posts mentioning the same entities. It is useful for `content discovery <discover.html#the-faceted-search-widget>`_.

.. image:: /images/wordlift-discover-navigator.png

Faceted search widget::

    [wl_faceted_search]

The Faceted Search widget can be used on entity pages to display and filter the posts related to the current and other entities. It is useful for `content discovery <discover.html#the-navigator-widget>`_.

.. image:: /images/wordlift-edit-entity-faceted-search-widget-frontend.gif

Entity cloud widget::

    [wl_cloud]

The **WordLift Entities Cloud Widget** is also available as a shortcode. The widget displays entities related to the current post/entity in a tag cloud.

.. image:: /images/wordlift-entities-cloud-widget.png

Glossary widget::

    [wl_cloud]  

The **Glossary** is a site-wide Widget that displays all the entities in alphabetical order. Here you can see an example of the `Semantic SEO Glossary <https://wordlift.io/blog/en/glossary>`_ 

.. _PHP date: http://php.net/manual/en/function.date.php
.. _PHP DateInterval format: http://php.net/manual/en/dateinterval.format.php

