:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the DampedSpringJoint2D.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_DampedSpringJoint2D:

DampedSpringJoint2D
===================

**Inherits:** :ref:`Joint2D<class_Joint2D>` **<** :ref:`Node2D<class_Node2D>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

2D 物理的阻尼弹簧约束。

描述
----

2D 物理的阻尼弹簧约束。这类似于总是想回到给定长度的弹簧关节。

属性
----

+---------------------------+--------------------------------------------------------------------+----------+
| :ref:`float<class_float>` | :ref:`damping<class_DampedSpringJoint2D_property_damping>`         | ``1.0``  |
+---------------------------+--------------------------------------------------------------------+----------+
| :ref:`float<class_float>` | :ref:`length<class_DampedSpringJoint2D_property_length>`           | ``50.0`` |
+---------------------------+--------------------------------------------------------------------+----------+
| :ref:`float<class_float>` | :ref:`rest_length<class_DampedSpringJoint2D_property_rest_length>` | ``0.0``  |
+---------------------------+--------------------------------------------------------------------+----------+
| :ref:`float<class_float>` | :ref:`stiffness<class_DampedSpringJoint2D_property_stiffness>`     | ``20.0`` |
+---------------------------+--------------------------------------------------------------------+----------+

属性说明
--------

.. _class_DampedSpringJoint2D_property_damping:

- :ref:`float<class_float>` **damping**

+-----------+--------------------+
| *Default* | ``1.0``            |
+-----------+--------------------+
| *Setter*  | set_damping(value) |
+-----------+--------------------+
| *Getter*  | get_damping()      |
+-----------+--------------------+

弹簧关节的阻尼比。值在 ``0`` 和 ``1`` 之间。当两个机构移动到不同的方向时，系统会尝试将它们再次对准弹簧轴。高的 ``damping`` 值迫使连接的机构更快地对齐。

----

.. _class_DampedSpringJoint2D_property_length:

- :ref:`float<class_float>` **length**

+-----------+-------------------+
| *Default* | ``50.0``          |
+-----------+-------------------+
| *Setter*  | set_length(value) |
+-----------+-------------------+
| *Getter*  | get_length()      |
+-----------+-------------------+

弹簧关节的最大长度。两个连接体不能超过这个值。

----

.. _class_DampedSpringJoint2D_property_rest_length:

- :ref:`float<class_float>` **rest_length**

+-----------+------------------------+
| *Default* | ``0.0``                |
+-----------+------------------------+
| *Setter*  | set_rest_length(value) |
+-----------+------------------------+
| *Getter*  | get_rest_length()      |
+-----------+------------------------+

当连接到弹簧关节的机构移动时，它们会拉伸或挤压它。关节总是尝试向这个长度调整。

----

.. _class_DampedSpringJoint2D_property_stiffness:

- :ref:`float<class_float>` **stiffness**

+-----------+----------------------+
| *Default* | ``20.0``             |
+-----------+----------------------+
| *Setter*  | set_stiffness(value) |
+-----------+----------------------+
| *Getter*  | get_stiffness()      |
+-----------+----------------------+

该值越大，连接在关节上的机构变形越小。关节对各机构施加一个相反的力，即刚度乘以与其静止长度的大小差的乘积。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
