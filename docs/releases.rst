Releases
===============
This section is dedicated to the latest *versions* of the plugin. Here you can keep track of everything that is happening with the developemnt of the plugin: read the *changelog* and discover *fixes and enhancements*.

**WordLift** developement is **open source** and we love to have you as contributor to both source code and issues; with your help we can make WordLift even better 🎉. Here is the link to `GitHub <https://github.com/insideout10/wordlift-plugin>`_ and here you can find `the guidelines for contributing <https://github.com/insideout10/wordlift-plugin/blob/develop/CONTRIBUTING.md>`_ to the repository. 

Just spotted any *creeping bug* or some *bothering issue*? Help us to smash it down: `report bugs and issues to us in detail on GitHub <https://github.com/insideout10/wordlift-plugin/issues/new>`_. Thank you 💙

WordLift 3.18 (2018-03-20) 
_____________

The WordLift 3.18 release is now available. We have introduced the new entity type for `Offer <http://docs.wordlift.io/en/latest/edit-entity.html#edit-a-offer>`_ and the support for the property `performer` on the entity type `Event <http://docs.wordlift.io/en/latest/edit-entity.html#edit-an-event>`_. The `glossary widget <http://docs.wordlift.io/en/latest/discover.html#the-glossary-widget>`_ has also been improved and it now supports a new option to let you display all the entities that belong to a specific WordPress Category. Above all, WordLift's Knowledge Graph got better 😉 the plugin now stores in RDF the link between entities and articles. 

`Download the latest release <https://wordpress.org/plugins/wordlift/>`_ now from WordPress.org or update it automatically from the administration panel of your website.

Have a look to the full `changelog on GitHub <https://github.com/insideout10/wordlift-plugin/issues?q=is%3Aopen+is%3Aissue+milestone%3A3.18>`_ for this release.

Read the latest article on our blog on how a `smarter knowledge graph can improve SEO on your website <https://wordlift.io/blog/en/knowledge-graph-seo/>`_.


WordLift 3.13.3 (2017-07-12) 
_____________

The WordLift 3.13.3 release is now available. The biggest news is that you can turn *on* and *off* WordLift’s analysis (and annotations) anytime you like. Say you are opening an article for a quick typo edit, you can now simply disable WordLift and avoid the analysis to run. Just click on the small arrow on the top-right corner of the WordLift’s widget. See how it works in the *.gif* below:

.. image:: /images/wl_toggle_3-13-3.gif

`Download the latest release <https://wordpress.org/plugins/wordlift/>`_ now from WordPress.org or update it automatically from the administration panel of your website.

Have a look to the full `changelog on GitHub <https://github.com/insideout10/wordlift-plugin/issues?utf8=%E2%9C%93&q=is%3Aclosed%20milestone%3A3.13.3%20>`_ for this release:

- Enhancement: #558: Link to the settings page in the message about unset key.
- Enhancement: #412: Add a toggle to disable WordLift’s analysis on certain pages/post.

WordLift 3.13.2 (2017-07-9) 
_____________

The WordLift 3.13.2 release is now available. The biggest news is that now *cron* has been replaced and the synchronization between WordPress and the Linked Data cloud is more reliable for everyone! We used *cron* to execute SPARQL queries from WordPress to the Linked Data Platform of WordLift. To replace *cron* we used an open source component originally developed by the team at TechCrunch 🙌. 

`Download the latest release <https://wordpress.org/plugins/wordlift/>`_ now from WordPress.org or update it automatically from the administration panel of your website.

Have a look to the full `changelog on GitHub <https://github.com/insideout10/wordlift-plugin/issues?utf8=%E2%9C%93&q=is%3Aclosed%20milestone%3A3.13.2%20>`_ for this release:

- Fix: #575: Cron is unreliable on some web sites.
- Fix: #576: Error 404 on a WooCommerce Product Page.
- Fix: #571: Faceted Search not displaying correctly.
- Fix: #568: Trying to get property of non-object in class-wordlift-sharethis-service.php.


Helpful links
_____________

* `WordLift Plugin on GitHub <https://github.com/insideout10/wordlift-plugin>`_ 

* `Contributing guidelines of the repository <https://github.com/insideout10/wordlift-plugin/blob/develop/CONTRIBUTING.md>`_ 

* `WordLift official website <https://wordlift.io>`_ 

* `The Plugin in the WordPress repository <https://wordpress.org/plugins/wordlift/#developers>`_

* `Translate WordLift in other languages <https://translate.wordpress.org/projects/wp-plugins/wordlift>`_



