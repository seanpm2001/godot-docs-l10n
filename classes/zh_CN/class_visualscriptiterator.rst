:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the VisualScriptIterator.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_VisualScriptIterator:

VisualScriptIterator
====================

**Inherits:** :ref:`VisualScriptNode<class_VisualScriptNode>` **<** :ref:`Resource<class_Resource>` **<** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

在给定输入中进行步骤项。

描述
----

这个节点在给定的输入中逐项进行。输入可以是任何序列数据类型，如\ :ref:`Array<class_Array>`\ 或\ :ref:`String<class_String>`\ 。当每个项被处理完后，执行传出\ ``exit`` 序列端口。

\ **Input Ports:**\ 

- Sequence: ``for (elem) in (input)``\ 

- Data (variant): ``input``\ 

\ **Output Ports:**\ 

- Sequence: ``each``\ 

- Sequence: ``exit``\ 

- Data (variant): ``elem``

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
