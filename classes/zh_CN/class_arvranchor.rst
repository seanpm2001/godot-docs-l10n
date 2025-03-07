:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the ARVRAnchor.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_ARVRAnchor:

ARVRAnchor
==========

**Inherits:** :ref:`Spatial<class_Spatial>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

AR空间中的锚点。

描述
----

``ARVRAnchor``\ 点是空间节点，它将AR平台识别的现实世界的位置映射到游戏世界中相应位置。例如，只要ARKit中的平面检测开启，ARKit就会识别并更新平面（桌子、地板等）的位置，并为其创建锚点。

此节点通过其特有ID映射到其中一个锚点。当你收到一个新锚点可用的信号时，在你的场景中，应该为该锚点添加这个节点。你可以预先定义节点并设置ID；节点将简单地保持在0,0,0，直到一个平面被识别。

请记住，只要启用了平面检测，锚的大小、位置和方向就会随着检测逻辑对外面真实世界的信息而更新，特别是在只有部分表面在视野中的情况下。

属性
----

+-----------------------+-------------------------------------------------------+-------+
| :ref:`int<class_int>` | :ref:`anchor_id<class_ARVRAnchor_property_anchor_id>` | ``1`` |
+-----------------------+-------------------------------------------------------+-------+

方法
----

+-------------------------------+-------------------------------------------------------------------------------------+
| :ref:`String<class_String>`   | :ref:`get_anchor_name<class_ARVRAnchor_method_get_anchor_name>` **(** **)** |const| |
+-------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`       | :ref:`get_is_active<class_ARVRAnchor_method_get_is_active>` **(** **)** |const|     |
+-------------------------------+-------------------------------------------------------------------------------------+
| :ref:`Mesh<class_Mesh>`       | :ref:`get_mesh<class_ARVRAnchor_method_get_mesh>` **(** **)** |const|               |
+-------------------------------+-------------------------------------------------------------------------------------+
| :ref:`Plane<class_Plane>`     | :ref:`get_plane<class_ARVRAnchor_method_get_plane>` **(** **)** |const|             |
+-------------------------------+-------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`get_size<class_ARVRAnchor_method_get_size>` **(** **)** |const|               |
+-------------------------------+-------------------------------------------------------------------------------------+

信号
----

.. _class_ARVRAnchor_signal_mesh_updated:

- **mesh_updated** **(** :ref:`Mesh<class_Mesh>` mesh **)**

当与锚点相关的网格发生变化或有可用的网格时触发。这对于不断\ ``Mesh_updated``\ 更新的拓扑结构尤为重要。

属性说明
--------

.. _class_ARVRAnchor_property_anchor_id:

- :ref:`int<class_int>` **anchor_id**

+-----------+----------------------+
| *Default* | ``1``                |
+-----------+----------------------+
| *Setter*  | set_anchor_id(value) |
+-----------+----------------------+
| *Getter*  | get_anchor_id()      |
+-----------+----------------------+

锚点的 ID。你可以在锚点本身存在之前设置它。第一个锚点的 ID 是 ``1``\ ，第二个锚点的 ID 是 ``2``\ ，以此类推。当锚点被移除时，引擎就可以将相应的 ID 分配给新的锚点。锚点“消失”的最常见情况是，AR 服务器识别出两个锚点代表同一平面的不同部分，并将它们合并。

方法说明
--------

.. _class_ARVRAnchor_method_get_anchor_name:

- :ref:`String<class_String>` **get_anchor_name** **(** **)** |const|

返回赋予此锚点的名称。

----

.. _class_ARVRAnchor_method_get_is_active:

- :ref:`bool<class_bool>` **get_is_active** **(** **)** |const|

如果正在跟踪锚点，则返回 ``true``\ ；如果当前没有已知具有此 ID 的锚点，则返回 ``false``\ 。

----

.. _class_ARVRAnchor_method_get_mesh:

- :ref:`Mesh<class_Mesh>` **get_mesh** **(** **)** |const|

如果由\ :ref:`ARVRInterface<class_ARVRInterface>`\ 提供，这将返回一个锚的网格对象。对于一个锚，这可以是一个与被追踪物体相关的形状，也可以是一个提供与锚相关的拓扑的网格，可以用于在表面上创建阴影/反射，或者用于生成碰撞形状。

----

.. _class_ARVRAnchor_method_get_plane:

- :ref:`Plane<class_Plane>` **get_plane** **(** **)** |const|

返回一个与我们的锚点对齐的平面；方便进行交集测试。

----

.. _class_ARVRAnchor_method_get_size:

- :ref:`Vector3<class_Vector3>` **get_size** **(** **)** |const|

返回检测到的平面的估计尺寸。比如当锚点与现实世界中的一张桌子有关时，这就是该桌子表面的估计尺寸。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
