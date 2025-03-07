:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the GLTFNode.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_GLTFNode:

GLTFNode
========

**Inherits:** :ref:`Resource<class_Resource>` **<** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`



Propiedades
----------------------

+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`camera<class_GLTFNode_property_camera>`           | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`PoolIntArray<class_PoolIntArray>` | :ref:`children<class_GLTFNode_property_children>`       | ``PoolIntArray(  )``                                |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`height<class_GLTFNode_property_height>`           | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`bool<class_bool>`                 | :ref:`joint<class_GLTFNode_property_joint>`             | ``false``                                           |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`light<class_GLTFNode_property_light>`             | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`mesh<class_GLTFNode_property_mesh>`               | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`parent<class_GLTFNode_property_parent>`           | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`Quat<class_Quat>`                 | :ref:`rotation<class_GLTFNode_property_rotation>`       | ``Quat( 0, 0, 0, 1 )``                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`Vector3<class_Vector3>`           | :ref:`scale<class_GLTFNode_property_scale>`             | ``Vector3( 1, 1, 1 )``                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`skeleton<class_GLTFNode_property_skeleton>`       | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`int<class_int>`                   | :ref:`skin<class_GLTFNode_property_skin>`               | ``-1``                                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`Vector3<class_Vector3>`           | :ref:`translation<class_GLTFNode_property_translation>` | ``Vector3( 0, 0, 0 )``                              |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+
| :ref:`Transform<class_Transform>`       | :ref:`xform<class_GLTFNode_property_xform>`             | ``Transform( 1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0 )`` |
+-----------------------------------------+---------------------------------------------------------+-----------------------------------------------------+

Descripciones de Propiedades
--------------------------------------------------------

.. _class_GLTFNode_property_camera:

- :ref:`int<class_int>` **camera**

+-----------+-------------------+
| *Default* | ``-1``            |
+-----------+-------------------+
| *Setter*  | set_camera(value) |
+-----------+-------------------+
| *Getter*  | get_camera()      |
+-----------+-------------------+

----

.. _class_GLTFNode_property_children:

- :ref:`PoolIntArray<class_PoolIntArray>` **children**

+-----------+----------------------+
| *Default* | ``PoolIntArray(  )`` |
+-----------+----------------------+
| *Setter*  | set_children(value)  |
+-----------+----------------------+
| *Getter*  | get_children()       |
+-----------+----------------------+

----

.. _class_GLTFNode_property_height:

- :ref:`int<class_int>` **height**

+-----------+-------------------+
| *Default* | ``-1``            |
+-----------+-------------------+
| *Setter*  | set_height(value) |
+-----------+-------------------+
| *Getter*  | get_height()      |
+-----------+-------------------+

----

.. _class_GLTFNode_property_joint:

- :ref:`bool<class_bool>` **joint**

+-----------+------------------+
| *Default* | ``false``        |
+-----------+------------------+
| *Setter*  | set_joint(value) |
+-----------+------------------+
| *Getter*  | get_joint()      |
+-----------+------------------+

----

.. _class_GLTFNode_property_light:

- :ref:`int<class_int>` **light**

+-----------+------------------+
| *Default* | ``-1``           |
+-----------+------------------+
| *Setter*  | set_light(value) |
+-----------+------------------+
| *Getter*  | get_light()      |
+-----------+------------------+

----

.. _class_GLTFNode_property_mesh:

- :ref:`int<class_int>` **mesh**

+-----------+-----------------+
| *Default* | ``-1``          |
+-----------+-----------------+
| *Setter*  | set_mesh(value) |
+-----------+-----------------+
| *Getter*  | get_mesh()      |
+-----------+-----------------+

----

.. _class_GLTFNode_property_parent:

- :ref:`int<class_int>` **parent**

+-----------+-------------------+
| *Default* | ``-1``            |
+-----------+-------------------+
| *Setter*  | set_parent(value) |
+-----------+-------------------+
| *Getter*  | get_parent()      |
+-----------+-------------------+

----

.. _class_GLTFNode_property_rotation:

- :ref:`Quat<class_Quat>` **rotation**

+-----------+------------------------+
| *Default* | ``Quat( 0, 0, 0, 1 )`` |
+-----------+------------------------+
| *Setter*  | set_rotation(value)    |
+-----------+------------------------+
| *Getter*  | get_rotation()         |
+-----------+------------------------+

----

.. _class_GLTFNode_property_scale:

- :ref:`Vector3<class_Vector3>` **scale**

+-----------+------------------------+
| *Default* | ``Vector3( 1, 1, 1 )`` |
+-----------+------------------------+
| *Setter*  | set_scale(value)       |
+-----------+------------------------+
| *Getter*  | get_scale()            |
+-----------+------------------------+

----

.. _class_GLTFNode_property_skeleton:

- :ref:`int<class_int>` **skeleton**

+-----------+---------------------+
| *Default* | ``-1``              |
+-----------+---------------------+
| *Setter*  | set_skeleton(value) |
+-----------+---------------------+
| *Getter*  | get_skeleton()      |
+-----------+---------------------+

----

.. _class_GLTFNode_property_skin:

- :ref:`int<class_int>` **skin**

+-----------+-----------------+
| *Default* | ``-1``          |
+-----------+-----------------+
| *Setter*  | set_skin(value) |
+-----------+-----------------+
| *Getter*  | get_skin()      |
+-----------+-----------------+

----

.. _class_GLTFNode_property_translation:

- :ref:`Vector3<class_Vector3>` **translation**

+-----------+------------------------+
| *Default* | ``Vector3( 0, 0, 0 )`` |
+-----------+------------------------+
| *Setter*  | set_translation(value) |
+-----------+------------------------+
| *Getter*  | get_translation()      |
+-----------+------------------------+

----

.. _class_GLTFNode_property_xform:

- :ref:`Transform<class_Transform>` **xform**

+-----------+-----------------------------------------------------+
| *Default* | ``Transform( 1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0 )`` |
+-----------+-----------------------------------------------------+
| *Setter*  | set_xform(value)                                    |
+-----------+-----------------------------------------------------+
| *Getter*  | get_xform()                                         |
+-----------+-----------------------------------------------------+

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
