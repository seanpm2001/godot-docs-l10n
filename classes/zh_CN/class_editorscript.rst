:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the EditorScript.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_EditorScript:

EditorScript
============

**Inherits:** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

可用于为编辑器添加扩展功能的基础脚本。

描述
----

扩展该类并实现其 :ref:`_run<class_EditorScript_method__run>` 方法的脚本可以在编辑器运行时通过脚本编辑器的 **File > Run** 菜单选项（或按 ``Ctrl+Shift+X``\ ）执行。这对于向 Godot添加自定义的编辑内功能很有用。对于更复杂的添加，可以考虑使用 :ref:`EditorPlugin<class_EditorPlugin>` 代替。

\ **注意：** 扩展脚本需要启用 ``tool`` 工具模式。

\ **示例脚本：**\ 

::

    tool
    extends EditorScript
    
    func _run():
        print("Hello from the Godot Editor!")

\ **注意：** 脚本在编辑器上下文中运行，这意味着输出在与编辑器一起启动的控制台窗口（stdout），而不是通常的 Godot **输出**\ 面板 。

方法
----

+-----------------------------------------------+--------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`_run<class_EditorScript_method__run>` **(** **)** |virtual|                                      |
+-----------------------------------------------+--------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`add_root_node<class_EditorScript_method_add_root_node>` **(** :ref:`Node<class_Node>` node **)** |
+-----------------------------------------------+--------------------------------------------------------------------------------------------------------+
| :ref:`EditorInterface<class_EditorInterface>` | :ref:`get_editor_interface<class_EditorScript_method_get_editor_interface>` **(** **)**                |
+-----------------------------------------------+--------------------------------------------------------------------------------------------------------+
| :ref:`Node<class_Node>`                       | :ref:`get_scene<class_EditorScript_method_get_scene>` **(** **)**                                      |
+-----------------------------------------------+--------------------------------------------------------------------------------------------------------+

方法说明
--------

.. _class_EditorScript_method__run:

- void **_run** **(** **)** |virtual|

当使用\ **文件 > 运行**\ 时，此方法由编辑器执行。

----

.. _class_EditorScript_method_add_root_node:

- void **add_root_node** **(** :ref:`Node<class_Node>` node **)**

将\ ``node``\ 添加为编辑器上下文中根节点的子级。

\ **警告：**\ 此方法的实现前处于禁用状态。

----

.. _class_EditorScript_method_get_editor_interface:

- :ref:`EditorInterface<class_EditorInterface>` **get_editor_interface** **(** **)**

返回\ :ref:`EditorInterface<class_EditorInterface>`\ 单例的实例。

----

.. _class_EditorScript_method_get_scene:

- :ref:`Node<class_Node>` **get_scene** **(** **)**

返回编辑器的当前活动场景。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
