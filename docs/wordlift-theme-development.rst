WordLift Theme Development
========

Who should read this 
_____________

This document is intended for Web Developers that would like to extend their themes to support WordLift's data model and features.

In the first paragraph we describe the WordLift data model, i.e. *how additional properties for entities are stored in WordPress*.

WordLift Data Model
_____________

1. WordLift Entities are **custom posts**;
2. Entity properties are managed as standard posts' metadata;
3. Entity types are managed through a `custom taxonomy <https://codex.wordpress.org/Taxonomies#Custom_Taxonomies>`_;
4. When a property references another entity:
	* Its value is the entity ID (if the entity is inside the same WordPress site),
	* Its value is the entity URI (if the entity is outside the WordPress site).
5. The 4Ws classification, i.e. the relationships among posts and entities, are stored in a custom table called *wl_relation_instances*.

Content Filtering - Available APIs
_____________

1. Standard WordPress methods (such as `get_posts <https://codex.wordpress.org/Template_Tags/get_posts>`_ and `get_post_meta <https://developer.wordpress.org/reference/functions/get_post_meta/>`_) can be used on entities;
2. WordLift's *Properties API* can be used to read/write entity properties using schema.org property names. See `here <https://github.com/insideout10/wordlift-plugin/blob/master/src/modules/core/wordlift_core_schema_api.php>`_; 
3. WordLift's *Relations API* can be used to access 4W relationships. See `here <https://github.com/insideout10/wordlift-plugin/blob/master/src/modules/core/wordlift_core_post_entity_relations.php>`_.


