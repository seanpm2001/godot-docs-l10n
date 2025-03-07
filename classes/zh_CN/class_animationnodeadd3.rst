:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the AnimationNodeAdd3.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_AnimationNodeAdd3:

AnimationNodeAdd3
=================

**Inherits:** :ref:`AnimationNode<class_AnimationNode>` **<** :ref:`Resource<class_Resource>` **<** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

在\ :ref:`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`\ 内部将三个动画中的两个动画相加。

描述
----

添加到 :ref:`AnimationNodeBlendTree<class_AnimationNodeBlendTree>` 的资源。根据 ``[-1.0, 1.0]`` 范围内的值，将三个动画中的两个动画加法混合在一起。

这个节点有三个输入。

- 要添加到基础动画中的动画

- 当混合量在\ ``[-1.0，0.0]``\ 范围内时，添加动画进行混合。

- 当混合量在\ ``[0.0，1.0]``\ 范围内时，添加动画进行混合

教程
----

- :doc:`AnimationTree <../tutorials/animation/animation_tree>`

- `Third Person Shooter Demo <https://godotengine.org/asset-library/asset/678>`__

属性
----

+-------------------------+----------------------------------------------------+-----------+
| :ref:`bool<class_bool>` | :ref:`sync<class_AnimationNodeAdd3_property_sync>` | ``false`` |
+-------------------------+----------------------------------------------------+-----------+

属性说明
--------

.. _class_AnimationNodeAdd3_property_sync:

- :ref:`bool<class_bool>` **sync**

+-----------+---------------------+
| *Default* | ``false``           |
+-----------+---------------------+
| *Setter*  | set_use_sync(value) |
+-----------+---------------------+
| *Getter*  | is_using_sync()     |
+-----------+---------------------+

如果\ ``true``\ ，在调用\ :ref:`AnimationNode.blend_input<class_AnimationNode_method_blend_input>`\ 时，将\ ``optimization`` to\ ``false``\ ，强制混合后的动画每一帧更新。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
