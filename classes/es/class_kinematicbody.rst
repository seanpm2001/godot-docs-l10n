:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the KinematicBody.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_KinematicBody:

KinematicBody
=============

**Inherits:** :ref:`PhysicsBody<class_PhysicsBody>` **<** :ref:`CollisionObject<class_CollisionObject>` **<** :ref:`Spatial<class_Spatial>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Nodo 3D del cuerpo cinético.

Descripción
----------------------

Kinematic bodies are special types of bodies that are meant to be user-controlled. They are not affected by physics at all; to other types of bodies, such as a character or a rigid body, these are the same as a static body. However, they have two main uses:

\ **Simulated motion:** When these bodies are moved manually, either from code or from an :ref:`AnimationPlayer<class_AnimationPlayer>` (with :ref:`AnimationPlayer.playback_process_mode<class_AnimationPlayer_property_playback_process_mode>` set to "physics"), the physics will automatically compute an estimate of their linear and angular velocity. This makes them very useful for moving platforms or other AnimationPlayer-controlled objects (like a door, a bridge that opens, etc).

\ **Kinematic characters:** KinematicBody also has an API for moving objects (the :ref:`move_and_collide<class_KinematicBody_method_move_and_collide>` and :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` methods) while performing collision tests. This makes them really useful to implement characters that collide against a world, but don't require advanced physics.

Tutoriales
--------------------

- :doc:`Kinematic character (2D) <../tutorials/physics/kinematic_character_2d>`

- `3D Kinematic Character Demo <https://godotengine.org/asset-library/asset/126>`__

- `3D Platformer Demo <https://godotengine.org/asset-library/asset/125>`__

- `3D Voxel Demo <https://godotengine.org/asset-library/asset/676>`__

- `Third Person Shooter Demo <https://godotengine.org/asset-library/asset/678>`__

Propiedades
----------------------

+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`axis_lock_motion_x<class_KinematicBody_property_axis_lock_motion_x>`         | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`axis_lock_motion_y<class_KinematicBody_property_axis_lock_motion_y>`         | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`axis_lock_motion_z<class_KinematicBody_property_axis_lock_motion_z>`         | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`float<class_float>` | :ref:`collision/safe_margin<class_KinematicBody_property_collision/safe_margin>`   | ``0.001`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`motion/sync_to_physics<class_KinematicBody_property_motion/sync_to_physics>` | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`move_lock_x<class_KinematicBody_property_move_lock_x>`                       | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`move_lock_y<class_KinematicBody_property_move_lock_y>`                       | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+
| :ref:`bool<class_bool>`   | :ref:`move_lock_z<class_KinematicBody_property_move_lock_z>`                       | ``false`` |
+---------------------------+------------------------------------------------------------------------------------+-----------+

Métodos
--------------

+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                             | :ref:`get_axis_lock<class_KinematicBody_method_get_axis_lock>` **(** :ref:`BodyAxis<enum_PhysicsServer_BodyAxis>` axis **)** |const|                                                                                                                                                                                                                                                                                                  |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`float<class_float>`                           | :ref:`get_floor_angle<class_KinematicBody_method_get_floor_angle>` **(** :ref:`Vector3<class_Vector3>` up_direction=Vector3( 0, 1, 0 ) **)** |const|                                                                                                                                                                                                                                                                                  |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`get_floor_normal<class_KinematicBody_method_get_floor_normal>` **(** **)** |const|                                                                                                                                                                                                                                                                                                                                              |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`get_floor_velocity<class_KinematicBody_method_get_floor_velocity>` **(** **)** |const|                                                                                                                                                                                                                                                                                                                                          |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`KinematicCollision<class_KinematicCollision>` | :ref:`get_last_slide_collision<class_KinematicBody_method_get_last_slide_collision>` **(** **)**                                                                                                                                                                                                                                                                                                                                      |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`KinematicCollision<class_KinematicCollision>` | :ref:`get_slide_collision<class_KinematicBody_method_get_slide_collision>` **(** :ref:`int<class_int>` slide_idx **)**                                                                                                                                                                                                                                                                                                                |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                               | :ref:`get_slide_count<class_KinematicBody_method_get_slide_count>` **(** **)** |const|                                                                                                                                                                                                                                                                                                                                                |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                             | :ref:`is_on_ceiling<class_KinematicBody_method_is_on_ceiling>` **(** **)** |const|                                                                                                                                                                                                                                                                                                                                                    |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                             | :ref:`is_on_floor<class_KinematicBody_method_is_on_floor>` **(** **)** |const|                                                                                                                                                                                                                                                                                                                                                        |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                             | :ref:`is_on_wall<class_KinematicBody_method_is_on_wall>` **(** **)** |const|                                                                                                                                                                                                                                                                                                                                                          |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`KinematicCollision<class_KinematicCollision>` | :ref:`move_and_collide<class_KinematicBody_method_move_and_collide>` **(** :ref:`Vector3<class_Vector3>` rel_vec, :ref:`bool<class_bool>` infinite_inertia=true, :ref:`bool<class_bool>` exclude_raycast_shapes=true, :ref:`bool<class_bool>` test_only=false **)**                                                                                                                                                                   |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` **(** :ref:`Vector3<class_Vector3>` linear_velocity, :ref:`Vector3<class_Vector3>` up_direction=Vector3( 0, 0, 0 ), :ref:`bool<class_bool>` stop_on_slope=false, :ref:`int<class_int>` max_slides=4, :ref:`float<class_float>` floor_max_angle=0.785398, :ref:`bool<class_bool>` infinite_inertia=true **)**                                                         |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>` **(** :ref:`Vector3<class_Vector3>` linear_velocity, :ref:`Vector3<class_Vector3>` snap, :ref:`Vector3<class_Vector3>` up_direction=Vector3( 0, 0, 0 ), :ref:`bool<class_bool>` stop_on_slope=false, :ref:`int<class_int>` max_slides=4, :ref:`float<class_float>` floor_max_angle=0.785398, :ref:`bool<class_bool>` infinite_inertia=true **)** |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                                | :ref:`set_axis_lock<class_KinematicBody_method_set_axis_lock>` **(** :ref:`BodyAxis<enum_PhysicsServer_BodyAxis>` axis, :ref:`bool<class_bool>` lock **)**                                                                                                                                                                                                                                                                            |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                             | :ref:`test_move<class_KinematicBody_method_test_move>` **(** :ref:`Transform<class_Transform>` from, :ref:`Vector3<class_Vector3>` rel_vec, :ref:`bool<class_bool>` infinite_inertia=true **)**                                                                                                                                                                                                                                       |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Descripciones de Propiedades
--------------------------------------------------------

.. _class_KinematicBody_property_axis_lock_motion_x:

- :ref:`bool<class_bool>` **axis_lock_motion_x**

+-----------+----------------------+
| *Default* | ``false``            |
+-----------+----------------------+
| *Setter*  | set_axis_lock(value) |
+-----------+----------------------+
| *Getter*  | get_axis_lock()      |
+-----------+----------------------+

Bloquea el movimiento del eje X del cuerpo.

----

.. _class_KinematicBody_property_axis_lock_motion_y:

- :ref:`bool<class_bool>` **axis_lock_motion_y**

+-----------+----------------------+
| *Default* | ``false``            |
+-----------+----------------------+
| *Setter*  | set_axis_lock(value) |
+-----------+----------------------+
| *Getter*  | get_axis_lock()      |
+-----------+----------------------+

Bloquea el movimiento del eje X del cuerpo.

----

.. _class_KinematicBody_property_axis_lock_motion_z:

- :ref:`bool<class_bool>` **axis_lock_motion_z**

+-----------+----------------------+
| *Default* | ``false``            |
+-----------+----------------------+
| *Setter*  | set_axis_lock(value) |
+-----------+----------------------+
| *Getter*  | get_axis_lock()      |
+-----------+----------------------+

Bloquea el movimiento del eje Z del cuerpo.

----

.. _class_KinematicBody_property_collision/safe_margin:

- :ref:`float<class_float>` **collision/safe_margin**

+-----------+------------------------+
| *Default* | ``0.001``              |
+-----------+------------------------+
| *Setter*  | set_safe_margin(value) |
+-----------+------------------------+
| *Getter*  | get_safe_margin()      |
+-----------+------------------------+

Extra margin used for collision recovery in motion functions (see :ref:`move_and_collide<class_KinematicBody_method_move_and_collide>`, :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>`, :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>`).

If the body is at least this close to another body, it will consider them to be colliding and will be pushed away before performing the actual motion.

A higher value means it's more flexible for detecting collision, which helps with consistently detecting walls and floors.

A lower value forces the collision algorithm to use more exact detection, so it can be used in cases that specifically require precision, e.g at very low scale to avoid visible jittering, or for stability with a stack of kinematic bodies.

----

.. _class_KinematicBody_property_motion/sync_to_physics:

- :ref:`bool<class_bool>` **motion/sync_to_physics**

+-----------+------------------------------+
| *Default* | ``false``                    |
+-----------+------------------------------+
| *Setter*  | set_sync_to_physics(value)   |
+-----------+------------------------------+
| *Getter*  | is_sync_to_physics_enabled() |
+-----------+------------------------------+

Si ``true``, el movimiento del cuerpo se sincronizará con el marco de la física. Esto es útil cuando se anima el movimiento a través de :ref:`AnimationPlayer<class_AnimationPlayer>`, por ejemplo en plataformas móviles. No uses **not** junto con las funciones :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` o :ref:`move_and_collide<class_KinematicBody_method_move_and_collide>`.

----

.. _class_KinematicBody_property_move_lock_x:

- :ref:`bool<class_bool>` **move_lock_x**

+-----------+----------------------+
| *Default* | ``false``            |
+-----------+----------------------+
| *Setter*  | set_axis_lock(value) |
+-----------+----------------------+
| *Getter*  | get_axis_lock()      |
+-----------+----------------------+

Lock the body's X axis movement. Deprecated alias for :ref:`axis_lock_motion_x<class_KinematicBody_property_axis_lock_motion_x>`.

----

.. _class_KinematicBody_property_move_lock_y:

- :ref:`bool<class_bool>` **move_lock_y**

+-----------+----------------------+
| *Default* | ``false``            |
+-----------+----------------------+
| *Setter*  | set_axis_lock(value) |
+-----------+----------------------+
| *Getter*  | get_axis_lock()      |
+-----------+----------------------+

Lock the body's Y axis movement. Deprecated alias for :ref:`axis_lock_motion_y<class_KinematicBody_property_axis_lock_motion_y>`.

----

.. _class_KinematicBody_property_move_lock_z:

- :ref:`bool<class_bool>` **move_lock_z**

+-----------+----------------------+
| *Default* | ``false``            |
+-----------+----------------------+
| *Setter*  | set_axis_lock(value) |
+-----------+----------------------+
| *Getter*  | get_axis_lock()      |
+-----------+----------------------+

Lock the body's Z axis movement. Deprecated alias for :ref:`axis_lock_motion_z<class_KinematicBody_property_axis_lock_motion_z>`.

Descripciones de Métodos
------------------------------------------------

.. _class_KinematicBody_method_get_axis_lock:

- :ref:`bool<class_bool>` **get_axis_lock** **(** :ref:`BodyAxis<enum_PhysicsServer_BodyAxis>` axis **)** |const|

Returns ``true`` if the specified ``axis`` is locked. See also :ref:`move_lock_x<class_KinematicBody_property_move_lock_x>`, :ref:`move_lock_y<class_KinematicBody_property_move_lock_y>` and :ref:`move_lock_z<class_KinematicBody_property_move_lock_z>`.

----

.. _class_KinematicBody_method_get_floor_angle:

- :ref:`float<class_float>` **get_floor_angle** **(** :ref:`Vector3<class_Vector3>` up_direction=Vector3( 0, 1, 0 ) **)** |const|

Returns the floor's collision angle at the last collision point according to ``up_direction``, which is ``Vector3.UP`` by default. This value is always positive and only valid after calling :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` and when :ref:`is_on_floor<class_KinematicBody_method_is_on_floor>` returns ``true``.

----

.. _class_KinematicBody_method_get_floor_normal:

- :ref:`Vector3<class_Vector3>` **get_floor_normal** **(** **)** |const|

Devuelve la normal de la superficie del suelo en el último punto de colisión. Sólo válido después de llamar a :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` o :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>` y cuando :ref:`is_on_floor<class_KinematicBody_method_is_on_floor>` devuelve ``true``.

----

.. _class_KinematicBody_method_get_floor_velocity:

- :ref:`Vector3<class_Vector3>` **get_floor_velocity** **(** **)** |const|

Devuelve la velocidad lineal del suelo en el último punto de colisión. Sólo es válido después de llamar a :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` o :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>` y cuando :ref:`is_on_floor<class_KinematicBody_method_is_on_floor>` devuelve ``true``.

----

.. _class_KinematicBody_method_get_last_slide_collision:

- :ref:`KinematicCollision<class_KinematicCollision>` **get_last_slide_collision** **(** **)**

Returns a :ref:`KinematicCollision<class_KinematicCollision>`, which contains information about the latest collision that occurred during the last call to :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>`.

----

.. _class_KinematicBody_method_get_slide_collision:

- :ref:`KinematicCollision<class_KinematicCollision>` **get_slide_collision** **(** :ref:`int<class_int>` slide_idx **)**

Returns a :ref:`KinematicCollision<class_KinematicCollision>`, which contains information about a collision that occurred during the last call to :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` or :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>`. Since the body can collide several times in a single call to :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>`, you must specify the index of the collision in the range 0 to (:ref:`get_slide_count<class_KinematicBody_method_get_slide_count>` - 1).

----

.. _class_KinematicBody_method_get_slide_count:

- :ref:`int<class_int>` **get_slide_count** **(** **)** |const|

Returns the number of times the body collided and changed direction during the last call to :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` or :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>`.

----

.. _class_KinematicBody_method_is_on_ceiling:

- :ref:`bool<class_bool>` **is_on_ceiling** **(** **)** |const|

Returns ``true`` if the body collided with the ceiling on the last call of :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` or :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>`. Otherwise, returns ``false``.

----

.. _class_KinematicBody_method_is_on_floor:

- :ref:`bool<class_bool>` **is_on_floor** **(** **)** |const|

Returns ``true`` if the body collided with the floor on the last call of :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` or :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>`. Otherwise, returns ``false``.

----

.. _class_KinematicBody_method_is_on_wall:

- :ref:`bool<class_bool>` **is_on_wall** **(** **)** |const|

Returns ``true`` if the body collided with a wall on the last call of :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` or :ref:`move_and_slide_with_snap<class_KinematicBody_method_move_and_slide_with_snap>`. Otherwise, returns ``false``.

----

.. _class_KinematicBody_method_move_and_collide:

- :ref:`KinematicCollision<class_KinematicCollision>` **move_and_collide** **(** :ref:`Vector3<class_Vector3>` rel_vec, :ref:`bool<class_bool>` infinite_inertia=true, :ref:`bool<class_bool>` exclude_raycast_shapes=true, :ref:`bool<class_bool>` test_only=false **)**

Moves the body along the vector ``rel_vec``. The body will stop if it collides. Returns a :ref:`KinematicCollision<class_KinematicCollision>`, which contains information about the collision when stopped, or when touching another body along the motion.

If ``test_only`` is ``true``, the body does not move but the would-be collision information is given.

----

.. _class_KinematicBody_method_move_and_slide:

- :ref:`Vector3<class_Vector3>` **move_and_slide** **(** :ref:`Vector3<class_Vector3>` linear_velocity, :ref:`Vector3<class_Vector3>` up_direction=Vector3( 0, 0, 0 ), :ref:`bool<class_bool>` stop_on_slope=false, :ref:`int<class_int>` max_slides=4, :ref:`float<class_float>` floor_max_angle=0.785398, :ref:`bool<class_bool>` infinite_inertia=true **)**

Moves the body along a vector. If the body collides with another, it will slide along the other body rather than stop immediately. If the other body is a ``KinematicBody`` or :ref:`RigidBody<class_RigidBody>`, it will also be affected by the motion of the other body. You can use this to make moving and rotating platforms, or to make nodes push other nodes.

This method should be used in :ref:`Node._physics_process<class_Node_method__physics_process>` (or in a method called by :ref:`Node._physics_process<class_Node_method__physics_process>`), as it uses the physics step's ``delta`` value automatically in calculations. Otherwise, the simulation will run at an incorrect speed.

\ ``linear_velocity`` is the velocity vector (typically meters per second). Unlike in :ref:`move_and_collide<class_KinematicBody_method_move_and_collide>`, you should *not* multiply it by ``delta`` — the physics engine handles applying the velocity.

\ ``up_direction`` is the up direction, used to determine what is a wall and what is a floor or a ceiling. If set to the default value of ``Vector3(0, 0, 0)``, everything is considered a wall.

If ``stop_on_slope`` is ``true``, body will not slide on slopes when you include gravity in ``linear_velocity`` and the body is standing still.

If the body collides, it will change direction a maximum of ``max_slides`` times before it stops.

\ ``floor_max_angle`` is the maximum angle (in radians) where a slope is still considered a floor (or a ceiling), rather than a wall. The default value equals 45 degrees.

If ``infinite_inertia`` is ``true``, body will be able to push :ref:`RigidBody<class_RigidBody>` nodes, but it won't also detect any collisions with them. If ``false``, it will interact with :ref:`RigidBody<class_RigidBody>` nodes like with :ref:`StaticBody<class_StaticBody>`.

Returns the ``linear_velocity`` vector, rotated and/or scaled if a slide collision occurred. To get detailed information about collisions that occurred, use :ref:`get_slide_collision<class_KinematicBody_method_get_slide_collision>`.

When the body touches a moving platform, the platform's velocity is automatically added to the body motion. If a collision occurs due to the platform's motion, it will always be first in the slide collisions.

----

.. _class_KinematicBody_method_move_and_slide_with_snap:

- :ref:`Vector3<class_Vector3>` **move_and_slide_with_snap** **(** :ref:`Vector3<class_Vector3>` linear_velocity, :ref:`Vector3<class_Vector3>` snap, :ref:`Vector3<class_Vector3>` up_direction=Vector3( 0, 0, 0 ), :ref:`bool<class_bool>` stop_on_slope=false, :ref:`int<class_int>` max_slides=4, :ref:`float<class_float>` floor_max_angle=0.785398, :ref:`bool<class_bool>` infinite_inertia=true **)**

Mueve el cuerpo mientras lo mantiene unido a las laderas. Similar al :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>`.

Mientras el vector ``snap`` esté en contacto con el suelo, el cuerpo permanecerá unido a la superficie. Esto significa que debes desactivar el snap para poder saltar, por ejemplo. Puedes hacerlo poniendo ``snap`` en ``(0, 0, 0)`` o usando :ref:`move_and_slide<class_KinematicBody_method_move_and_slide>` en su lugar.

----

.. _class_KinematicBody_method_set_axis_lock:

- void **set_axis_lock** **(** :ref:`BodyAxis<enum_PhysicsServer_BodyAxis>` axis, :ref:`bool<class_bool>` lock **)**

Locks or unlocks the specified ``axis`` depending on the value of ``lock``. See also :ref:`move_lock_x<class_KinematicBody_property_move_lock_x>`, :ref:`move_lock_y<class_KinematicBody_property_move_lock_y>` and :ref:`move_lock_z<class_KinematicBody_property_move_lock_z>`.

----

.. _class_KinematicBody_method_test_move:

- :ref:`bool<class_bool>` **test_move** **(** :ref:`Transform<class_Transform>` from, :ref:`Vector3<class_Vector3>` rel_vec, :ref:`bool<class_bool>` infinite_inertia=true **)**

Checks for collisions without moving the body. Virtually sets the node's position, scale and rotation to that of the given :ref:`Transform<class_Transform>`, then tries to move the body along the vector ``rel_vec``. Returns ``true`` if a collision would stop the body from moving along the whole path.

Use :ref:`move_and_collide<class_KinematicBody_method_move_and_collide>` instead for detecting collision with touching bodies.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
