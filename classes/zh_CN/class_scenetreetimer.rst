:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the SceneTreeTimer.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_SceneTreeTimer:

SceneTreeTimer
==============

**Inherits:** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

一次性定时器。

描述
----

由场景树管理的一次性定时器，它在完成时发\ :ref:`timeout<class_SceneTreeTimer_signal_timeout>` 信号。请参阅 :ref:`SceneTree.create_timer<class_SceneTree_method_create_timer>`\ 。

与 :ref:`Timer<class_Timer>` 相反，它不需要实例化节点。常用于创建一次性的延迟定时器，如下面的例子：

::

    func some_function():
        print("计时器开始。")
        yield(get_tree().create_timer(1.0), "timeout")
        print("计时器结束。")

时间结束后，该计时器将被自动释放。

属性
----

+---------------------------+-----------------------------------------------------------+
| :ref:`float<class_float>` | :ref:`time_left<class_SceneTreeTimer_property_time_left>` |
+---------------------------+-----------------------------------------------------------+

信号
----

.. _class_SceneTreeTimer_signal_timeout:

- **timeout** **(** **)**

当计时器到 0 时发出。

属性说明
--------

.. _class_SceneTreeTimer_property_time_left:

- :ref:`float<class_float>` **time_left**

+----------+----------------------+
| *Setter* | set_time_left(value) |
+----------+----------------------+
| *Getter* | get_time_left()      |
+----------+----------------------+

剩余时间（单位为秒）。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
