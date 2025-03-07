:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the AnimatedSprite.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_AnimatedSprite:

AnimatedSprite
==============

**Inherits:** :ref:`Node2D<class_Node2D>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

可以使用多个纹理进行动画处理的 Sprite 节点。

描述
----

动画通过一个 :ref:`SpriteFrames<class_SpriteFrames>` 资源创建，而该资源可以通过动画帧面板在编辑器中配置。

\ **注意：**\ 您可以通过创建附加的带有 ``_normal`` 后缀的 :ref:`SpriteFrames<class_SpriteFrames>` 资源来关联一组法线贴图。例如，如有 2 个 :ref:`SpriteFrames<class_SpriteFrames>` 资源 ``run`` 和 ``run_normal``\ ，将使 ``run`` 动画使用该法线贴图。

教程
----

- :doc:`2D Sprite animation <../tutorials/2d/2d_sprite_animation>`

- `2D Dodge The Creeps Demo <https://godotengine.org/asset-library/asset/515>`__

属性
----

+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`String<class_String>`             | :ref:`animation<class_AnimatedSprite_property_animation>`     | ``"default"``       |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`                 | :ref:`centered<class_AnimatedSprite_property_centered>`       | ``true``            |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`                 | :ref:`flip_h<class_AnimatedSprite_property_flip_h>`           | ``false``           |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`                 | :ref:`flip_v<class_AnimatedSprite_property_flip_v>`           | ``false``           |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`int<class_int>`                   | :ref:`frame<class_AnimatedSprite_property_frame>`             | ``0``               |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`SpriteFrames<class_SpriteFrames>` | :ref:`frames<class_AnimatedSprite_property_frames>`           |                     |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`Vector2<class_Vector2>`           | :ref:`offset<class_AnimatedSprite_property_offset>`           | ``Vector2( 0, 0 )`` |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`                 | :ref:`playing<class_AnimatedSprite_property_playing>`         | ``false``           |
+-----------------------------------------+---------------------------------------------------------------+---------------------+
| :ref:`float<class_float>`               | :ref:`speed_scale<class_AnimatedSprite_property_speed_scale>` | ``1.0``             |
+-----------------------------------------+---------------------------------------------------------------+---------------------+

方法
----

+------+----------------------------------------------------------------------------------------------------------------------------------------+
| void | :ref:`play<class_AnimatedSprite_method_play>` **(** :ref:`String<class_String>` anim="", :ref:`bool<class_bool>` backwards=false **)** |
+------+----------------------------------------------------------------------------------------------------------------------------------------+
| void | :ref:`stop<class_AnimatedSprite_method_stop>` **(** **)**                                                                              |
+------+----------------------------------------------------------------------------------------------------------------------------------------+

信号
----

.. _class_AnimatedSprite_signal_animation_finished:

- **animation_finished** **(** **)**

动画结束时（播放最后一帧时）发出。如果动画正在循环播放，则每次绘制最后一帧时都会发出此信号。

----

.. _class_AnimatedSprite_signal_frame_changed:

- **frame_changed** **(** **)**

当\ :ref:`frame<class_AnimatedSprite_property_frame>`\ 更改时发出。

属性说明
--------

.. _class_AnimatedSprite_property_animation:

- :ref:`String<class_String>` **animation**

+-----------+----------------------+
| *Default* | ``"default"``        |
+-----------+----------------------+
| *Setter*  | set_animation(value) |
+-----------+----------------------+
| *Getter*  | get_animation()      |
+-----------+----------------------+

来自 ``frames`` 资源的当前动画。如果这个值发生变化，\ ``frame`` 计数器会被重置。

----

.. _class_AnimatedSprite_property_centered:

- :ref:`bool<class_bool>` **centered**

+-----------+---------------------+
| *Default* | ``true``            |
+-----------+---------------------+
| *Setter*  | set_centered(value) |
+-----------+---------------------+
| *Getter*  | is_centered()       |
+-----------+---------------------+

为 ``true`` 时纹理将被居中。

----

.. _class_AnimatedSprite_property_flip_h:

- :ref:`bool<class_bool>` **flip_h**

+-----------+-------------------+
| *Default* | ``false``         |
+-----------+-------------------+
| *Setter*  | set_flip_h(value) |
+-----------+-------------------+
| *Getter*  | is_flipped_h()    |
+-----------+-------------------+

为 ``true`` 时纹理将被水平翻转。

----

.. _class_AnimatedSprite_property_flip_v:

- :ref:`bool<class_bool>` **flip_v**

+-----------+-------------------+
| *Default* | ``false``         |
+-----------+-------------------+
| *Setter*  | set_flip_v(value) |
+-----------+-------------------+
| *Getter*  | is_flipped_v()    |
+-----------+-------------------+

为 ``true`` 时纹理将被垂直翻转。

----

.. _class_AnimatedSprite_property_frame:

- :ref:`int<class_int>` **frame**

+-----------+------------------+
| *Default* | ``0``            |
+-----------+------------------+
| *Setter*  | set_frame(value) |
+-----------+------------------+
| *Getter*  | get_frame()      |
+-----------+------------------+

显示的动画帧的索引。

----

.. _class_AnimatedSprite_property_frames:

- :ref:`SpriteFrames<class_SpriteFrames>` **frames**

+----------+--------------------------+
| *Setter* | set_sprite_frames(value) |
+----------+--------------------------+
| *Getter* | get_sprite_frames()      |
+----------+--------------------------+

包含动画的 :ref:`SpriteFrames<class_SpriteFrames>` 资源。

----

.. _class_AnimatedSprite_property_offset:

- :ref:`Vector2<class_Vector2>` **offset**

+-----------+---------------------+
| *Default* | ``Vector2( 0, 0 )`` |
+-----------+---------------------+
| *Setter*  | set_offset(value)   |
+-----------+---------------------+
| *Getter*  | get_offset()        |
+-----------+---------------------+

纹理的绘图偏移量。

----

.. _class_AnimatedSprite_property_playing:

- :ref:`bool<class_bool>` **playing**

+-----------+--------------------+
| *Default* | ``false``          |
+-----------+--------------------+
| *Setter*  | set_playing(value) |
+-----------+--------------------+
| *Getter*  | is_playing()       |
+-----------+--------------------+

如果 ``true``\ ，则表示当前正在播放 :ref:`animation<class_AnimatedSprite_property_animation>`\ 。

----

.. _class_AnimatedSprite_property_speed_scale:

- :ref:`float<class_float>` **speed_scale**

+-----------+------------------------+
| *Default* | ``1.0``                |
+-----------+------------------------+
| *Setter*  | set_speed_scale(value) |
+-----------+------------------------+
| *Getter*  | get_speed_scale()      |
+-----------+------------------------+

动画速度乘以此值。

方法说明
--------

.. _class_AnimatedSprite_method_play:

- void **play** **(** :ref:`String<class_String>` anim="", :ref:`bool<class_bool>` backwards=false **)**

播放由 ``anim`` 指定的播放。如果没有指定 ``anim`` 参数，则播放当前动画。 如果 ``backwards`` 为 ``true`` ，则倒序播放动画。

----

.. _class_AnimatedSprite_method_stop:

- void **stop** **(** **)**

停止播放当前动画（不会重置帧计数器）。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
