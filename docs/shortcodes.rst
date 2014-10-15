Widget Shortcodes
_________________

WordLift widgets can be inserted in a post or page to give a rich visual presentation of the entities populating the blog. As the blog grows and entities are created and mentioned, the widgets update their content without intervention from the editor.

Chord widget::

    [wl-chord width=... height=... main_color=... depth=... global=...]
    
.. image:: /images/wordlift-shortcodes-chord.png
Visualizes relations between entities, starting from the current post and the entities mentioned in it.

width
    *(optional)* Width of the chord. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the chord. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

main_color
    *(optional)* The chord's *base* color.

depth
    *(optional)* Maximum distance to travel in the entity graph in order to populate the chord. A small number limits the exploration in the neighborhood of the main entity.

global
    *(optional)* When *global=true* the main entity of the chord is not the current post, but the most mentioned entity in the blog.
    
Timeline widget::
    
    [wl-timeline width=... height=... global=...]
    
.. image:: /images/wordlift-shortcodes-timeline.png
Displays a navigable list of ordered Event entities. The window on top shows details on the clicked Events.

width
    *(optional)* Width of the timeline. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the timeline. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

global
    *(optional)* By default the timeline displays events (or events related to places) mentioned in the current post. When *global=true* the timeline displays events mentioned in the latest posts.

Geomap widget::

    [wl-geomap width=... height=... global=...]
    
.. image:: /images/wordlift-shortcodes-geomap.png    
Displays Place entities on a map. Each Place has its own marker with a popup containing thumbnail and link.
    
width
    *(optional)* Width of the geomap. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).
    
height
    *(optional)* Height of the geomap. Can be expressed in pixels or percentages (e.g. *120px* or *70%*).

global
    *(optional)* By default the geomap displays places mentioned in the current post. When *global=true* the geomap displays all places mentioned in the blog.

Related posts widget::

    [wl-related-posts]

Offers links to semantic-related posts in the blog.








Shortcodes
==========

WordLift provides several useful shortcodes to provide enhanced visualization on your web site.

Entity Shortcodes
_________________


Load entity data::

    [wl_entity_view uri=... suffix=...][/wl_entity_view]

The URI of the entity is determined by combining the *uri* defined in the shortcode and the current address path.

uri
    The *base* URI for remote resources (e.g. http://data.redlink.io/353/salzburgerland/

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


Displays a duration::

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


.. _PHP date: http://php.net/manual/en/function.date.php
.. _PHP DateInterval format: http://php.net/manual/en/dateinterval.format.php



