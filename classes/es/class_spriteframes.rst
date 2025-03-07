:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the SpriteFrames.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_SpriteFrames:

SpriteFrames
============

**Inherits:** :ref:`Resource<class_Resource>` **<** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

Sprite frame library for AnimatedSprite.

Descripción
----------------------

Sprite frame library for :ref:`AnimatedSprite<class_AnimatedSprite>`. Contains frames and animation data for playback.

\ **Note:** You can associate a set of normal maps by creating additional ``SpriteFrames`` resources with a ``_normal`` suffix. For example, having 2 ``SpriteFrames`` resources ``run`` and ``run_normal`` will make it so the ``run`` animation uses the normal map.

Propiedades
----------------------

+---------------------------+---------------------------------------------------+
| :ref:`Array<class_Array>` | :ref:`frames<class_SpriteFrames_property_frames>` |
+---------------------------+---------------------------------------------------+

Métodos
--------------

+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`add_animation<class_SpriteFrames_method_add_animation>` **(** :ref:`String<class_String>` anim **)**                                                                    |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`add_frame<class_SpriteFrames_method_add_frame>` **(** :ref:`String<class_String>` anim, :ref:`Texture<class_Texture>` frame, :ref:`int<class_int>` at_position=-1 **)** |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`clear<class_SpriteFrames_method_clear>` **(** :ref:`String<class_String>` anim **)**                                                                                    |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`clear_all<class_SpriteFrames_method_clear_all>` **(** **)**                                                                                                             |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                       | :ref:`get_animation_loop<class_SpriteFrames_method_get_animation_loop>` **(** :ref:`String<class_String>` anim **)** |const|                                                  |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolStringArray<class_PoolStringArray>` | :ref:`get_animation_names<class_SpriteFrames_method_get_animation_names>` **(** **)** |const|                                                                                 |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`float<class_float>`                     | :ref:`get_animation_speed<class_SpriteFrames_method_get_animation_speed>` **(** :ref:`String<class_String>` anim **)** |const|                                                |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Texture<class_Texture>`                 | :ref:`get_frame<class_SpriteFrames_method_get_frame>` **(** :ref:`String<class_String>` anim, :ref:`int<class_int>` idx **)** |const|                                         |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                         | :ref:`get_frame_count<class_SpriteFrames_method_get_frame_count>` **(** :ref:`String<class_String>` anim **)** |const|                                                        |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                       | :ref:`has_animation<class_SpriteFrames_method_has_animation>` **(** :ref:`String<class_String>` anim **)** |const|                                                            |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`remove_animation<class_SpriteFrames_method_remove_animation>` **(** :ref:`String<class_String>` anim **)**                                                              |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`remove_frame<class_SpriteFrames_method_remove_frame>` **(** :ref:`String<class_String>` anim, :ref:`int<class_int>` idx **)**                                           |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`rename_animation<class_SpriteFrames_method_rename_animation>` **(** :ref:`String<class_String>` anim, :ref:`String<class_String>` newname **)**                         |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`set_animation_loop<class_SpriteFrames_method_set_animation_loop>` **(** :ref:`String<class_String>` anim, :ref:`bool<class_bool>` loop **)**                            |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`set_animation_speed<class_SpriteFrames_method_set_animation_speed>` **(** :ref:`String<class_String>` anim, :ref:`float<class_float>` speed **)**                       |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`set_frame<class_SpriteFrames_method_set_frame>` **(** :ref:`String<class_String>` anim, :ref:`int<class_int>` idx, :ref:`Texture<class_Texture>` txt **)**              |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Descripciones de Propiedades
--------------------------------------------------------

.. _class_SpriteFrames_property_frames:

- :ref:`Array<class_Array>` **frames**

La propiedad de compatibilidad, siempre equivale a una array vacío.

Descripciones de Métodos
------------------------------------------------

.. _class_SpriteFrames_method_add_animation:

- void **add_animation** **(** :ref:`String<class_String>` anim **)**

Añade una nueva animación a la biblioteca.

----

.. _class_SpriteFrames_method_add_frame:

- void **add_frame** **(** :ref:`String<class_String>` anim, :ref:`Texture<class_Texture>` frame, :ref:`int<class_int>` at_position=-1 **)**

Añade un fotograma a la animación dada.

----

.. _class_SpriteFrames_method_clear:

- void **clear** **(** :ref:`String<class_String>` anim **)**

Elimina todos los fotogramas de la animación dada.

----

.. _class_SpriteFrames_method_clear_all:

- void **clear_all** **(** **)**

Elimina todas las animaciones. Se creará una animación "por defecto".

----

.. _class_SpriteFrames_method_get_animation_loop:

- :ref:`bool<class_bool>` **get_animation_loop** **(** :ref:`String<class_String>` anim **)** |const|

Returns ``true`` if the given animation is configured to loop when it finishes playing. Otherwise, returns ``false``.

----

.. _class_SpriteFrames_method_get_animation_names:

- :ref:`PoolStringArray<class_PoolStringArray>` **get_animation_names** **(** **)** |const|

Devuelve un array que contiene los nombres asociados a cada animación. Los valores se colocan en orden alfabético.

----

.. _class_SpriteFrames_method_get_animation_speed:

- :ref:`float<class_float>` **get_animation_speed** **(** :ref:`String<class_String>` anim **)** |const|

La velocidad de la animación en fotogramas por segundo.

----

.. _class_SpriteFrames_method_get_frame:

- :ref:`Texture<class_Texture>` **get_frame** **(** :ref:`String<class_String>` anim, :ref:`int<class_int>` idx **)** |const|

Devuelve el fotograma seleccionado de la animación.

----

.. _class_SpriteFrames_method_get_frame_count:

- :ref:`int<class_int>` **get_frame_count** **(** :ref:`String<class_String>` anim **)** |const|

Devuelve el número de fotogramas de la animación.

----

.. _class_SpriteFrames_method_has_animation:

- :ref:`bool<class_bool>` **has_animation** **(** :ref:`String<class_String>` anim **)** |const|

Si ``true``, la animación nombrada existe.

----

.. _class_SpriteFrames_method_remove_animation:

- void **remove_animation** **(** :ref:`String<class_String>` anim **)**

Elimina la animación dada.

----

.. _class_SpriteFrames_method_remove_frame:

- void **remove_frame** **(** :ref:`String<class_String>` anim, :ref:`int<class_int>` idx **)**

Elimina el fotograma seleccionado de la animación.

----

.. _class_SpriteFrames_method_rename_animation:

- void **rename_animation** **(** :ref:`String<class_String>` anim, :ref:`String<class_String>` newname **)**

Cambia el nombre de la animación a ``newname``.

----

.. _class_SpriteFrames_method_set_animation_loop:

- void **set_animation_loop** **(** :ref:`String<class_String>` anim, :ref:`bool<class_bool>` loop **)**

Si ``true``, la animación se repetirá.

----

.. _class_SpriteFrames_method_set_animation_speed:

- void **set_animation_speed** **(** :ref:`String<class_String>` anim, :ref:`float<class_float>` speed **)**

La velocidad de la animación en fotogramas por segundo.

----

.. _class_SpriteFrames_method_set_frame:

- void **set_frame** **(** :ref:`String<class_String>` anim, :ref:`int<class_int>` idx, :ref:`Texture<class_Texture>` txt **)**

Establece la textura del fotograma dado.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
