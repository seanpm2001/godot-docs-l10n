:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the StaticBody2D.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_StaticBody2D:

StaticBody2D
============

**Inherits:** :ref:`PhysicsBody2D<class_PhysicsBody2D>` **<** :ref:`CollisionObject2D<class_CollisionObject2D>` **<** :ref:`Node2D<class_Node2D>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Cuerpo estático para la física 2D.

Descripción
----------------------

Cuerpo estático para la física 2D. Un StaticBody2D es un cuerpo que no está destinado a moverse. Es ideal para implementar objetos en el entorno, como paredes o plataformas.

Además, se puede establecer una velocidad lineal o angular constante para el cuerpo estático, que afectará a los cuerpos que colisionen como si se movieran (por ejemplo, una cinta transportadora).

Propiedades
----------------------

+-----------------------------------------------+-----------------------------------------------------------------------------------------+---------------------+
| :ref:`float<class_float>`                     | :ref:`bounce<class_StaticBody2D_property_bounce>`                                       |                     |
+-----------------------------------------------+-----------------------------------------------------------------------------------------+---------------------+
| :ref:`float<class_float>`                     | :ref:`constant_angular_velocity<class_StaticBody2D_property_constant_angular_velocity>` | ``0.0``             |
+-----------------------------------------------+-----------------------------------------------------------------------------------------+---------------------+
| :ref:`Vector2<class_Vector2>`                 | :ref:`constant_linear_velocity<class_StaticBody2D_property_constant_linear_velocity>`   | ``Vector2( 0, 0 )`` |
+-----------------------------------------------+-----------------------------------------------------------------------------------------+---------------------+
| :ref:`float<class_float>`                     | :ref:`friction<class_StaticBody2D_property_friction>`                                   |                     |
+-----------------------------------------------+-----------------------------------------------------------------------------------------+---------------------+
| :ref:`PhysicsMaterial<class_PhysicsMaterial>` | :ref:`physics_material_override<class_StaticBody2D_property_physics_material_override>` |                     |
+-----------------------------------------------+-----------------------------------------------------------------------------------------+---------------------+

Descripciones de Propiedades
--------------------------------------------------------

.. _class_StaticBody2D_property_bounce:

- :ref:`float<class_float>` **bounce**

+----------+-------------------+
| *Setter* | set_bounce(value) |
+----------+-------------------+
| *Getter* | get_bounce()      |
+----------+-------------------+

The body's bounciness. Values range from ``0`` (no bounce) to ``1`` (full bounciness).

Deprecated, use :ref:`PhysicsMaterial.bounce<class_PhysicsMaterial_property_bounce>` instead via :ref:`physics_material_override<class_StaticBody2D_property_physics_material_override>`.

----

.. _class_StaticBody2D_property_constant_angular_velocity:

- :ref:`float<class_float>` **constant_angular_velocity**

+-----------+--------------------------------------+
| *Default* | ``0.0``                              |
+-----------+--------------------------------------+
| *Setter*  | set_constant_angular_velocity(value) |
+-----------+--------------------------------------+
| *Getter*  | get_constant_angular_velocity()      |
+-----------+--------------------------------------+

La velocidad angular constante del cuerpo. Esto no rota el cuerpo, sino que afecta a los cuerpos en colisión, como si estuviera rotando.

----

.. _class_StaticBody2D_property_constant_linear_velocity:

- :ref:`Vector2<class_Vector2>` **constant_linear_velocity**

+-----------+-------------------------------------+
| *Default* | ``Vector2( 0, 0 )``                 |
+-----------+-------------------------------------+
| *Setter*  | set_constant_linear_velocity(value) |
+-----------+-------------------------------------+
| *Getter*  | get_constant_linear_velocity()      |
+-----------+-------------------------------------+

La velocidad lineal constante del cuerpo. Esto no mueve el cuerpo, sino que afecta a los cuerpos en colisión, como si se moviera.

----

.. _class_StaticBody2D_property_friction:

- :ref:`float<class_float>` **friction**

+----------+---------------------+
| *Setter* | set_friction(value) |
+----------+---------------------+
| *Getter* | get_friction()      |
+----------+---------------------+

The body's friction. Values range from ``0`` (no friction) to ``1`` (full friction).

Deprecated, use :ref:`PhysicsMaterial.friction<class_PhysicsMaterial_property_friction>` instead via :ref:`physics_material_override<class_StaticBody2D_property_physics_material_override>`.

----

.. _class_StaticBody2D_property_physics_material_override:

- :ref:`PhysicsMaterial<class_PhysicsMaterial>` **physics_material_override**

+----------+--------------------------------------+
| *Setter* | set_physics_material_override(value) |
+----------+--------------------------------------+
| *Getter* | get_physics_material_override()      |
+----------+--------------------------------------+

El material de la física se sobreescribe para el cuerpo.

Si se asigna un material a esta propiedad, se utilizará en lugar de cualquier otro material de física, como por ejemplo uno heredado.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
