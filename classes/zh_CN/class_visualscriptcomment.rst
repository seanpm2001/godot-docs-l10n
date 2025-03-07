:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the VisualScriptComment.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_VisualScriptComment:

VisualScriptComment
===================

**Inherits:** :ref:`VisualScriptNode<class_VisualScriptNode>` **<** :ref:`Resource<class_Resource>` **<** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

用于注释脚本的可视化脚本节点。

描述
----

可视化脚本节点，用于显示脚本中的注释，以便记录代码。

注释节点可以调整大小，以便包含一组节点。

属性
----

+-------------------------------+--------------------------------------------------------------------+-------------------------+
| :ref:`String<class_String>`   | :ref:`description<class_VisualScriptComment_property_description>` | ``""``                  |
+-------------------------------+--------------------------------------------------------------------+-------------------------+
| :ref:`Vector2<class_Vector2>` | :ref:`size<class_VisualScriptComment_property_size>`               | ``Vector2( 150, 150 )`` |
+-------------------------------+--------------------------------------------------------------------+-------------------------+
| :ref:`String<class_String>`   | :ref:`title<class_VisualScriptComment_property_title>`             | ``"Comment"``           |
+-------------------------------+--------------------------------------------------------------------+-------------------------+

属性说明
--------

.. _class_VisualScriptComment_property_description:

- :ref:`String<class_String>` **description**

+-----------+------------------------+
| *Default* | ``""``                 |
+-----------+------------------------+
| *Setter*  | set_description(value) |
+-----------+------------------------+
| *Getter*  | get_description()      |
+-----------+------------------------+

注释节点内的文本。

----

.. _class_VisualScriptComment_property_size:

- :ref:`Vector2<class_Vector2>` **size**

+-----------+-------------------------+
| *Default* | ``Vector2( 150, 150 )`` |
+-----------+-------------------------+
| *Setter*  | set_size(value)         |
+-----------+-------------------------+
| *Getter*  | get_size()              |
+-----------+-------------------------+

注释节点的大小（以像素为单位）。

----

.. _class_VisualScriptComment_property_title:

- :ref:`String<class_String>` **title**

+-----------+------------------+
| *Default* | ``"Comment"``    |
+-----------+------------------+
| *Setter*  | set_title(value) |
+-----------+------------------+
| *Getter*  | get_title()      |
+-----------+------------------+

注释节点的标题。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
