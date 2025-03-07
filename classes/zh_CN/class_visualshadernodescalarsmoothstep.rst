:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the VisualShaderNodeScalarSmoothStep.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_VisualShaderNodeScalarSmoothStep:

VisualShaderNodeScalarSmoothStep
================================

**Inherits:** :ref:`VisualShaderNode<class_VisualShaderNode>` **<** :ref:`Resource<class_Resource>` **<** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

在可视化着色器图中计算一个标量的SmoothStep函数。

描述
----

在着色器语言中转换成\ ``smoothstep(edge0, edge1, x)``\ 。

如果\ ``x``\ 小于\ ``edge0``\ ，返回\ ``0.0``\ ；如果\ ``x``\ 大于\ ``edge1``\ ，返回\ ``1.0``\ 。否则返回值在\ ``0.0``\ 和\ ``1.0``\ 之间使用Hermite多项式进行插值。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
