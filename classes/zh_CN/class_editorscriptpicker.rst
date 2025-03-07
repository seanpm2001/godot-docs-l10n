:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the EditorScriptPicker.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_EditorScriptPicker:

EditorScriptPicker
==================

**Inherits:** :ref:`EditorResourcePicker<class_EditorResourcePicker>` **<** :ref:`HBoxContainer<class_HBoxContainer>` **<** :ref:`BoxContainer<class_BoxContainer>` **<** :ref:`Container<class_Container>` **<** :ref:`Control<class_Control>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Godot 编辑器的控件，用于选择节点 :ref:`Node<class_Node>` 的脚本 ``script`` 属性。

描述
----

与 :ref:`EditorResourcePicker<class_EditorResourcePicker>` 类似，这个 :ref:`Control<class_Control>` 节点在编辑器的检查器面板中使用，但只用于编辑 :ref:`Node<class_Node>` 的 ``script`` 属性。创建包含所有可能子类型的新资源的默认选项 被替换为打开“附加节点脚本”对话框的专用按钮。可以与 :ref:`EditorInspectorPlugin<class_EditorInspectorPlugin>` 一起使用以重新创建相同的行为。

\ **注意：** 你必须设置 :ref:`script_owner<class_EditorScriptPicker_property_script_owner>` 才能让自定义的上下文菜单项发挥作用。

属性
----

+-------------------------+---------------------------------------------------------------------+
| :ref:`Node<class_Node>` | :ref:`script_owner<class_EditorScriptPicker_property_script_owner>` |
+-------------------------+---------------------------------------------------------------------+

属性说明
--------

.. _class_EditorScriptPicker_property_script_owner:

- :ref:`Node<class_Node>` **script_owner**

+----------+-------------------------+
| *Setter* | set_script_owner(value) |
+----------+-------------------------+
| *Getter* | get_script_owner()      |
+----------+-------------------------+

持有被编辑资源的脚本属性的所有者 :ref:`Node<class_Node>`\ 。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
