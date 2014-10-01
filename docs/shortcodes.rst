Shortcodes
==========

WordLift provides several useful shortcodes to provide enhanced visualization on your web site.

Entity Shortcodes
_________________


Load entity data:

    [wl_entity_view uri=... suffix=...][/wl_entity_view]

The URI of the entity is determined by combining the *uri* defined in the shortcode and the current address path.

uri
    The *base* URI for remote resources (e.g. http://data.redlink.io/353/salzburgerland/

suffix
    *(optional)* The suffix for remote requests (e.g. '.json')


Display the value of a property:

    [wl_entity_property name=... language=...]

It must be used inside a *wl_entity_view*.

name
    The full property name (e.g. http://www.w3.org/2000/01/rdf-schema#label)

language
    *(optional)* The language (e.g. 'en'). If it's not specified, the shortcode looks for a value without a language.


Display an image (using the *img* tag):

    [wl_entity_image name=...]

It must be used inside a *wl_entity_view*.

name
    The full property name (e.g. http://schema.org/image)


Display a date:

    [wl_entity_date name=... format=...]

name
    The full property name (e.g. http://www.w3.org/2002/12/cal#dtstart)

format
    *(optional, default 'Y m d')* The format to apply to the date (follows the PHP convention, see `PHP date`_ for more information).


Displays a duration:

    [wl_entity_duration name=... format=...]

name
    The full property name (e.g. http://www.w3.org/2002/12/cal#dtstart)

format
    *(optional, default '%d day(s), %h hour(s)')* The format to apply to the duration (follows the PHP convention, see `PHP DateInterval format`_ for more information).


Example:

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

