:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the GridMap.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_GridMap:

GridMap
=======

**Inherits:** :ref:`Spatial<class_Spatial>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

基于3D贴图格地图(3D tile-based maps)的节点。

描述
----

GridMap允许你以交互方式将meshes网格放置在网格上。它既可以在编辑器中进行，也可以从脚本中进行，这可以帮助你在游戏中创建关卡编辑器。

GridMaps使用\ :ref:`MeshLibrary<class_MeshLibrary>`\ ，其中包含了一个图块的列表。每一个图块都是一个带有材质的网格，加上可选的碰撞和导航形状。

GridMap包含一个单元格的集合。每个网格单元指的是\ :ref:`MeshLibrary<class_MeshLibrary>`\ 中的一个图块。地图中的所有单元都有相同的尺寸。

在内部，GridMap被分割成一个松散的八边形集合，以便有效地进行渲染和物理处理。每个八角形都有相同的尺寸，可以包含多个单元。

\ **注意：**\ GridMap 没有扩展 :ref:`VisualInstance<class_VisualInstance>`\ ，因此无法根据 :ref:`VisualInstance.layers<class_VisualInstance_property_layers>` 进行隐藏或剔除遮挡。如果你让灯光不影响第一层，整个 GridMap 就都不会被相关的灯光照亮。

教程
----

- :doc:`Using gridmaps <../tutorials/3d/using_gridmaps>`

- `3D Platformer Demo <https://godotengine.org/asset-library/asset/125>`__

- `3D Kinematic Character Demo <https://godotengine.org/asset-library/asset/126>`__

属性
----

+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`bool<class_bool>`               | :ref:`cell_center_x<class_GridMap_property_cell_center_x>`           | ``true``               |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`bool<class_bool>`               | :ref:`cell_center_y<class_GridMap_property_cell_center_y>`           | ``true``               |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`bool<class_bool>`               | :ref:`cell_center_z<class_GridMap_property_cell_center_z>`           | ``true``               |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`int<class_int>`                 | :ref:`cell_octant_size<class_GridMap_property_cell_octant_size>`     | ``8``                  |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`float<class_float>`             | :ref:`cell_scale<class_GridMap_property_cell_scale>`                 | ``1.0``                |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`Vector3<class_Vector3>`         | :ref:`cell_size<class_GridMap_property_cell_size>`                   | ``Vector3( 2, 2, 2 )`` |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`int<class_int>`                 | :ref:`collision_layer<class_GridMap_property_collision_layer>`       | ``1``                  |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`int<class_int>`                 | :ref:`collision_mask<class_GridMap_property_collision_mask>`         | ``1``                  |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`MeshLibrary<class_MeshLibrary>` | :ref:`mesh_library<class_GridMap_property_mesh_library>`             |                        |
+---------------------------------------+----------------------------------------------------------------------+------------------------+
| :ref:`bool<class_bool>`               | :ref:`use_in_baked_light<class_GridMap_property_use_in_baked_light>` | ``false``              |
+---------------------------------------+----------------------------------------------------------------------+------------------------+

方法
----

+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`clear<class_GridMap_method_clear>` **(** **)**                                                                                                                                                            |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`clear_baked_meshes<class_GridMap_method_clear_baked_meshes>` **(** **)**                                                                                                                                  |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`RID<class_RID>`         | :ref:`get_bake_mesh_instance<class_GridMap_method_get_bake_mesh_instance>` **(** :ref:`int<class_int>` idx **)**                                                                                                |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`     | :ref:`get_bake_meshes<class_GridMap_method_get_bake_meshes>` **(** **)**                                                                                                                                        |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`         | :ref:`get_cell_item<class_GridMap_method_get_cell_item>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** |const|                                                          |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`         | :ref:`get_cell_item_orientation<class_GridMap_method_get_cell_item_orientation>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** |const|                                  |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`       | :ref:`get_collision_layer_bit<class_GridMap_method_get_collision_layer_bit>` **(** :ref:`int<class_int>` bit **)** |const|                                                                                      |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`       | :ref:`get_collision_mask_bit<class_GridMap_method_get_collision_mask_bit>` **(** :ref:`int<class_int>` bit **)** |const|                                                                                        |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`     | :ref:`get_meshes<class_GridMap_method_get_meshes>` **(** **)**                                                                                                                                                  |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`     | :ref:`get_used_cells<class_GridMap_method_get_used_cells>` **(** **)** |const|                                                                                                                                  |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`make_baked_meshes<class_GridMap_method_make_baked_meshes>` **(** :ref:`bool<class_bool>` gen_lightmap_uv=false, :ref:`float<class_float>` lightmap_uv_texel_size=0.1 **)**                                |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`map_to_world<class_GridMap_method_map_to_world>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** |const|                                                            |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`resource_changed<class_GridMap_method_resource_changed>` **(** :ref:`Resource<class_Resource>` resource **)**                                                                                             |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`set_cell_item<class_GridMap_method_set_cell_item>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z, :ref:`int<class_int>` item, :ref:`int<class_int>` orientation=0 **)** |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`set_clip<class_GridMap_method_set_clip>` **(** :ref:`bool<class_bool>` enabled, :ref:`bool<class_bool>` clipabove=true, :ref:`int<class_int>` floor=0, Vector3.Axis axis=0 **)**                          |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`set_collision_layer_bit<class_GridMap_method_set_collision_layer_bit>` **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**                                                               |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`set_collision_mask_bit<class_GridMap_method_set_collision_mask_bit>` **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**                                                                 |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`world_to_map<class_GridMap_method_world_to_map>` **(** :ref:`Vector3<class_Vector3>` pos **)** |const|                                                                                                    |
+-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

信号
----

.. _class_GridMap_signal_cell_size_changed:

- **cell_size_changed** **(** :ref:`Vector3<class_Vector3>` cell_size **)**

当 :ref:`cell_size<class_GridMap_property_cell_size>` 改变时触发。

常量
----

.. _class_GridMap_constant_INVALID_CELL_ITEM:

- **INVALID_CELL_ITEM** = **-1** --- 可以在 :ref:`set_cell_item<class_GridMap_method_set_cell_item>` 中清除单元格（或在 :ref:`get_cell_item<class_GridMap_method_get_cell_item>` 中重新代表一个空的单元格）的无效单元格。

属性说明
--------

.. _class_GridMap_property_cell_center_x:

- :ref:`bool<class_bool>` **cell_center_x**

+-----------+---------------------+
| *Default* | ``true``            |
+-----------+---------------------+
| *Setter*  | set_center_x(value) |
+-----------+---------------------+
| *Getter*  | get_center_x()      |
+-----------+---------------------+

如果\ ``true``\ ，则网格项以X轴为中心。

----

.. _class_GridMap_property_cell_center_y:

- :ref:`bool<class_bool>` **cell_center_y**

+-----------+---------------------+
| *Default* | ``true``            |
+-----------+---------------------+
| *Setter*  | set_center_y(value) |
+-----------+---------------------+
| *Getter*  | get_center_y()      |
+-----------+---------------------+

如果为 ``true``\ ，则网格项以 Y 轴为中心。

----

.. _class_GridMap_property_cell_center_z:

- :ref:`bool<class_bool>` **cell_center_z**

+-----------+---------------------+
| *Default* | ``true``            |
+-----------+---------------------+
| *Setter*  | set_center_z(value) |
+-----------+---------------------+
| *Getter*  | get_center_z()      |
+-----------+---------------------+

如果为 ``true``\ ，则网格项以 Z 轴为中心。

----

.. _class_GridMap_property_cell_octant_size:

- :ref:`int<class_int>` **cell_octant_size**

+-----------+------------------------+
| *Default* | ``8``                  |
+-----------+------------------------+
| *Setter*  | set_octant_size(value) |
+-----------+------------------------+
| *Getter*  | get_octant_size()      |
+-----------+------------------------+

每个八分圆的大小以单元格的数量衡量。这适用于三个轴(XYZ)。

----

.. _class_GridMap_property_cell_scale:

- :ref:`float<class_float>` **cell_scale**

+-----------+-----------------------+
| *Default* | ``1.0``               |
+-----------+-----------------------+
| *Setter*  | set_cell_scale(value) |
+-----------+-----------------------+
| *Getter*  | get_cell_scale()      |
+-----------+-----------------------+

单元格项目的比例。

这不会影响网格单元本身的大小，只会影响其中的项目。这可用于使单元格项目与其邻居重叠。

----

.. _class_GridMap_property_cell_size:

- :ref:`Vector3<class_Vector3>` **cell_size**

+-----------+------------------------+
| *Default* | ``Vector3( 2, 2, 2 )`` |
+-----------+------------------------+
| *Setter*  | set_cell_size(value)   |
+-----------+------------------------+
| *Getter*  | get_cell_size()        |
+-----------+------------------------+

网格单元的尺寸。

这并不影响网格的尺寸大小。参阅\ :ref:`cell_scale<class_GridMap_property_cell_scale>`\ 。

----

.. _class_GridMap_property_collision_layer:

- :ref:`int<class_int>` **collision_layer**

+-----------+----------------------------+
| *Default* | ``1``                      |
+-----------+----------------------------+
| *Setter*  | set_collision_layer(value) |
+-----------+----------------------------+
| *Getter*  | get_collision_layer()      |
+-----------+----------------------------+

这个GridMap所处的物理层。

Gridmap作为静态体，意味着它们不会受到重力或是其他力的影响。它们只会受到其他与它们碰撞的物理体的影响。

----

.. _class_GridMap_property_collision_mask:

- :ref:`int<class_int>` **collision_mask**

+-----------+---------------------------+
| *Default* | ``1``                     |
+-----------+---------------------------+
| *Setter*  | set_collision_mask(value) |
+-----------+---------------------------+
| *Getter*  | get_collision_mask()      |
+-----------+---------------------------+

The physics layers this GridMap detects collisions in. See `Collision layers and masks <../tutorials/physics/physics_introduction.html#collision-layers-and-masks>`__ in the documentation for more information.

----

.. _class_GridMap_property_mesh_library:

- :ref:`MeshLibrary<class_MeshLibrary>` **mesh_library**

+----------+-------------------------+
| *Setter* | set_mesh_library(value) |
+----------+-------------------------+
| *Getter* | get_mesh_library()      |
+----------+-------------------------+

指定的\ :ref:`MeshLibrary<class_MeshLibrary>`\ 。

----

.. _class_GridMap_property_use_in_baked_light:

- :ref:`bool<class_bool>` **use_in_baked_light**

+-----------+-------------------------------+
| *Default* | ``false``                     |
+-----------+-------------------------------+
| *Setter*  | set_use_in_baked_light(value) |
+-----------+-------------------------------+
| *Getter*  | get_use_in_baked_light()      |
+-----------+-------------------------------+

控制此 GridMap 是否会在 :ref:`BakedLightmap<class_BakedLightmap>` 中烘焙。

方法说明
--------

.. _class_GridMap_method_clear:

- void **clear** **(** **)**

清除所有单元格。

----

.. _class_GridMap_method_clear_baked_meshes:

- void **clear_baked_meshes** **(** **)**

----

.. _class_GridMap_method_get_bake_mesh_instance:

- :ref:`RID<class_RID>` **get_bake_mesh_instance** **(** :ref:`int<class_int>` idx **)**

----

.. _class_GridMap_method_get_bake_meshes:

- :ref:`Array<class_Array>` **get_bake_meshes** **(** **)**

返回当前GridMap中存在的所有烘焙网格的\ :ref:`ArrayMesh<class_ArrayMesh>`\ 和\ :ref:`Transform<class_Transform>`\ 引用的数组。

----

.. _class_GridMap_method_get_cell_item:

- :ref:`int<class_int>` **get_cell_item** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** |const|

:ref:`MeshLibrary<class_MeshLibrary>` 项目索引位于基于网格的 X、Y 和 Z 坐标处。如果单元格为空，则返回 :ref:`INVALID_CELL_ITEM<class_GridMap_constant_INVALID_CELL_ITEM>`\ 。

----

.. _class_GridMap_method_get_cell_item_orientation:

- :ref:`int<class_int>` **get_cell_item_orientation** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** |const|

单元格在基于网格的 X、Y 和 Z 坐标处的方向。如果单元格为空，则返回 -1。

----

.. _class_GridMap_method_get_collision_layer_bit:

- :ref:`bool<class_bool>` **get_collision_layer_bit** **(** :ref:`int<class_int>` bit **)** |const|

返回\ :ref:`collision_layer<class_GridMap_property_collision_layer>`\ 上的一个单独像素点。

----

.. _class_GridMap_method_get_collision_mask_bit:

- :ref:`bool<class_bool>` **get_collision_mask_bit** **(** :ref:`int<class_int>` bit **)** |const|

返回\ :ref:`collision_mask<class_GridMap_property_collision_mask>`\ 上的一个独立像素。

----

.. _class_GridMap_method_get_meshes:

- :ref:`Array<class_Array>` **get_meshes** **(** **)**

返回对应于网格中非空单元格的 :ref:`Transform<class_Transform>` 和 :ref:`Mesh<class_Mesh>` 引用数组。变换在世界空间中指定。

----

.. _class_GridMap_method_get_used_cells:

- :ref:`Array<class_Array>` **get_used_cells** **(** **)** |const|

返回一个包含网格中非空单元格坐标的 :ref:`Vector3<class_Vector3>` 数组。

----

.. _class_GridMap_method_make_baked_meshes:

- void **make_baked_meshes** **(** :ref:`bool<class_bool>` gen_lightmap_uv=false, :ref:`float<class_float>` lightmap_uv_texel_size=0.1 **)**

----

.. _class_GridMap_method_map_to_world:

- :ref:`Vector3<class_Vector3>` **map_to_world** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** |const|

返回一个网格单元在GridMap本地坐标空间中的位置。

----

.. _class_GridMap_method_resource_changed:

- void **resource_changed** **(** :ref:`Resource<class_Resource>` resource **)**

----

.. _class_GridMap_method_set_cell_item:

- void **set_cell_item** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z, :ref:`int<class_int>` item, :ref:`int<class_int>` orientation=0 **)**

设置由基于网格的 X、Y 和 Z 坐标引用的单元格的网格索引。

负的项目索引将清除单元格，例如 :ref:`INVALID_CELL_ITEM<class_GridMap_constant_INVALID_CELL_ITEM>`\ 。

或者，可以传递项目的方向。相关有效的方向值，请参阅 :ref:`Basis.get_orthogonal_index<class_Basis_method_get_orthogonal_index>`\ 。

----

.. _class_GridMap_method_set_clip:

- void **set_clip** **(** :ref:`bool<class_bool>` enabled, :ref:`bool<class_bool>` clipabove=true, :ref:`int<class_int>` floor=0, Vector3.Axis axis=0 **)**

----

.. _class_GridMap_method_set_collision_layer_bit:

- void **set_collision_layer_bit** **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**

在\ :ref:`collision_layer<class_GridMap_property_collision_layer>`\ 上设置独立像素。

----

.. _class_GridMap_method_set_collision_mask_bit:

- void **set_collision_mask_bit** **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**

在\ :ref:`collision_mask<class_GridMap_property_collision_mask>`\ 上设置独立像素。

----

.. _class_GridMap_method_world_to_map:

- :ref:`Vector3<class_Vector3>` **world_to_map** **(** :ref:`Vector3<class_Vector3>` pos **)** |const|

返回包含给定点的网格单元的坐标。

\ ``pos``\ 应该在GridMap的本地坐标空间中。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
