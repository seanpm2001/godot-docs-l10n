:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the ResourceFormatLoader.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_ResourceFormatLoader:

ResourceFormatLoader
====================

**Inherits:** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

从文件中加载特定资源类型。

描述
----

Godot使用ResourceFormatLoaders在编辑器或导出的游戏中加载资源。它们通过\ :ref:`ResourceLoader<class_ResourceLoader>`\ 单例自动查询，或者在加载具有内部依赖性的资源时被查询。每个文件类型可以作为不同的资源类型加载，因此在引擎中注册了多个ResourceFormatLoaders。

扩展这个类允许你定义你自己的加载器。请确保尊重文档中的返回类型和值。你应该给它一个带有\ ``class_name``\ 的全局类名，这样它才能被注册。像内置的ResourceFormatLoaders一样，它将在加载其处理的类型的资源时被自动调用。你也可以实现一个\ :ref:`ResourceFormatSaver<class_ResourceFormatSaver>`\ 。

\ **注意：** 如果你需要的资源类型存在，但Godot无法加载其格式，你也可以扩展\ :ref:`EditorImportPlugin<class_EditorImportPlugin>`\ 。选择一种方式而不是另一种方式，取决于该格式是否适合于最终导出的游戏。例如，最好先把\ ``.png``\ 纹理导入为\ ``.stex``\ （\ :ref:`StreamTexture<class_StreamTexture>`\ ），这样它们在显卡上的加载效率会更好。

方法
----

+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`get_dependencies<class_ResourceFormatLoader_method_get_dependencies>` **(** :ref:`String<class_String>` path, :ref:`String<class_String>` add_types **)** |virtual|     |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolStringArray<class_PoolStringArray>` | :ref:`get_recognized_extensions<class_ResourceFormatLoader_method_get_recognized_extensions>` **(** **)** |virtual|                                                           |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`String<class_String>`                   | :ref:`get_resource_type<class_ResourceFormatLoader_method_get_resource_type>` **(** :ref:`String<class_String>` path **)** |virtual|                                          |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                       | :ref:`handles_type<class_ResourceFormatLoader_method_handles_type>` **(** :ref:`String<class_String>` typename **)** |virtual|                                                |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Variant<class_Variant>`                 | :ref:`load<class_ResourceFormatLoader_method_load>` **(** :ref:`String<class_String>` path, :ref:`String<class_String>` original_path **)** |virtual|                         |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                         | :ref:`rename_dependencies<class_ResourceFormatLoader_method_rename_dependencies>` **(** :ref:`String<class_String>` path, :ref:`String<class_String>` renames **)** |virtual| |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

方法说明
--------

.. _class_ResourceFormatLoader_method_get_dependencies:

- void **get_dependencies** **(** :ref:`String<class_String>` path, :ref:`String<class_String>` add_types **)** |virtual|

如果实现，则获取给定资源的依赖项。如果 ``add_types`` 是 ``true``\ ，路径应该附加 ``::TypeName``\ ，其中 ``TypeName`` 是依赖的类名。

\ **注意：** :ref:`ClassDB<class_ClassDB>` 不知道脚本定义的自定义资源类型，因此您可能只为它们返回 ``"Resource"``\ 。

----

.. _class_ResourceFormatLoader_method_get_recognized_extensions:

- :ref:`PoolStringArray<class_PoolStringArray>` **get_recognized_extensions** **(** **)** |virtual|

获取该加载器能够读取的文件的扩展名列表。

----

.. _class_ResourceFormatLoader_method_get_resource_type:

- :ref:`String<class_String>` **get_resource_type** **(** :ref:`String<class_String>` path **)** |virtual|

获取与给定路径相关的资源的类名。如果加载器不能处理它，它应该返回\ ``""``\ 。

\ **注意：** :ref:`ClassDB<class_ClassDB>` 不知道脚本定义的自定义资源类型，因此您可能只为它们返回 ``"Resource"``\ 。

----

.. _class_ResourceFormatLoader_method_handles_type:

- :ref:`bool<class_bool>` **handles_type** **(** :ref:`String<class_String>` typename **)** |virtual|

说明这个加载器可以加载哪个资源类。

\ **注意:** :ref:`ClassDB<class_ClassDB>` 不知道脚本定义的自定义资源类型，因此您可以只为它们处理 ``"Resource"``\ 。

----

.. _class_ResourceFormatLoader_method_load:

- :ref:`Variant<class_Variant>` **load** **(** :ref:`String<class_String>` path, :ref:`String<class_String>` original_path **)** |virtual|

当引擎发现这个加载器是兼容的，就会加载一个资源。如果加载的资源是导入的结果，\ ``original_path``\ 将针对源文件。成功时返回一个\ :ref:`Resource<class_Resource>`\ 对象，失败时返回一个\ :ref:`Error<enum_@GlobalScope_Error>`\ 常量。

----

.. _class_ResourceFormatLoader_method_rename_dependencies:

- :ref:`int<class_int>` **rename_dependencies** **(** :ref:`String<class_String>` path, :ref:`String<class_String>` renames **)** |virtual|

如果实现，重命名给定资源中的依赖项并保存它。 ``renames`` 是一个将旧的依赖路径映射到新的路径的 ``{ String => String }``\ 的字典 。

成功时返回 :ref:`@GlobalScope.OK<class_@GlobalScope_constant_OK>`\ ，失败时返回 :ref:`Error<enum_@GlobalScope_Error>` 常量。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
