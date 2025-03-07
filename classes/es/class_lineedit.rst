:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the LineEdit.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_LineEdit:

LineEdit
========

**Inherits:** :ref:`Control<class_Control>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Control que proporciona la edición de string de una sola línea.

Descripción
----------------------

LineEdit provides a single-line string editor, used for text fields.

It features many built-in shortcuts which will always be available (``Ctrl`` here maps to ``Command`` on macOS):

- Ctrl + C: Copy

- Ctrl + X: Cut

- Ctrl + V or Ctrl + Y: Paste/"yank"

- Ctrl + Z: Undo

- Ctrl + Shift + Z: Redo

- Ctrl + U: Delete text from the cursor position to the beginning of the line

- Ctrl + K: Delete text from the cursor position to the end of the line

- Ctrl + A: Select all text

- Up/Down arrow: Move the cursor to the beginning/end of the line

On macOS, some extra keyboard shortcuts are available:

- Ctrl + F: Like the right arrow key, move the cursor one character right

- Ctrl + B: Like the left arrow key, move the cursor one character left

- Ctrl + P: Like the up arrow key, move the cursor to the previous line

- Ctrl + N: Like the down arrow key, move the cursor to the next line

- Ctrl + D: Like the Delete key, delete the character on the right side of cursor

- Ctrl + H: Like the Backspace key, delete the character on the left side of the cursor

- Command + Left arrow: Like the Home key, move the cursor to the beginning of the line

- Command + Right arrow: Like the End key, move the cursor to the end of the line

Propiedades
----------------------

+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`Align<enum_LineEdit_Align>`            | :ref:`align<class_LineEdit_property_align>`                                       | ``0``                                                                               |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`caret_blink<class_LineEdit_property_caret_blink>`                           | ``false``                                                                           |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`float<class_float>`                    | :ref:`caret_blink_speed<class_LineEdit_property_caret_blink_speed>`               | ``0.65``                                                                            |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                        | :ref:`caret_position<class_LineEdit_property_caret_position>`                     | ``0``                                                                               |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`clear_button_enabled<class_LineEdit_property_clear_button_enabled>`         | ``false``                                                                           |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`context_menu_enabled<class_LineEdit_property_context_menu_enabled>`         | ``true``                                                                            |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`editable<class_LineEdit_property_editable>`                                 | ``true``                                                                            |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`expand_to_text_length<class_LineEdit_property_expand_to_text_length>`       | ``false``                                                                           |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`FocusMode<enum_Control_FocusMode>`     | focus_mode                                                                        | ``2`` (overrides :ref:`Control<class_Control_property_focus_mode>`)                 |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                        | :ref:`max_length<class_LineEdit_property_max_length>`                             | ``0``                                                                               |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`CursorShape<enum_Control_CursorShape>` | mouse_default_cursor_shape                                                        | ``1`` (overrides :ref:`Control<class_Control_property_mouse_default_cursor_shape>`) |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`float<class_float>`                    | :ref:`placeholder_alpha<class_LineEdit_property_placeholder_alpha>`               | ``0.6``                                                                             |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`String<class_String>`                  | :ref:`placeholder_text<class_LineEdit_property_placeholder_text>`                 | ``""``                                                                              |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`Texture<class_Texture>`                | :ref:`right_icon<class_LineEdit_property_right_icon>`                             |                                                                                     |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`secret<class_LineEdit_property_secret>`                                     | ``false``                                                                           |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`String<class_String>`                  | :ref:`secret_character<class_LineEdit_property_secret_character>`                 | ``"*"``                                                                             |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`selecting_enabled<class_LineEdit_property_selecting_enabled>`               | ``true``                                                                            |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`shortcut_keys_enabled<class_LineEdit_property_shortcut_keys_enabled>`       | ``true``                                                                            |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`String<class_String>`                  | :ref:`text<class_LineEdit_property_text>`                                         | ``""``                                                                              |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                      | :ref:`virtual_keyboard_enabled<class_LineEdit_property_virtual_keyboard_enabled>` | ``true``                                                                            |
+----------------------------------------------+-----------------------------------------------------------------------------------+-------------------------------------------------------------------------------------+

Métodos
--------------

+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`append_at_cursor<class_LineEdit_method_append_at_cursor>` **(** :ref:`String<class_String>` text **)**                         |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`clear<class_LineEdit_method_clear>` **(** **)**                                                                                |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`delete_char_at_cursor<class_LineEdit_method_delete_char_at_cursor>` **(** **)**                                                |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`delete_text<class_LineEdit_method_delete_text>` **(** :ref:`int<class_int>` from_column, :ref:`int<class_int>` to_column **)** |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`deselect<class_LineEdit_method_deselect>` **(** **)**                                                                          |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PopupMenu<class_PopupMenu>` | :ref:`get_menu<class_LineEdit_method_get_menu>` **(** **)** |const|                                                                  |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`             | :ref:`get_scroll_offset<class_LineEdit_method_get_scroll_offset>` **(** **)** |const|                                                |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`menu_option<class_LineEdit_method_menu_option>` **(** :ref:`int<class_int>` option **)**                                       |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`select<class_LineEdit_method_select>` **(** :ref:`int<class_int>` from=0, :ref:`int<class_int>` to=-1 **)**                    |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| void                              | :ref:`select_all<class_LineEdit_method_select_all>` **(** **)**                                                                      |
+-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+

Propiedades del Theme
------------------------------------------

+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`clear_button_color<class_LineEdit_theme_color_clear_button_color>`                 | ``Color( 0.88, 0.88, 0.88, 1 )``   |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`clear_button_color_pressed<class_LineEdit_theme_color_clear_button_color_pressed>` | ``Color( 1, 1, 1, 1 )``            |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`cursor_color<class_LineEdit_theme_color_cursor_color>`                             | ``Color( 0.94, 0.94, 0.94, 1 )``   |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`font_color<class_LineEdit_theme_color_font_color>`                                 | ``Color( 0.88, 0.88, 0.88, 1 )``   |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`font_color_selected<class_LineEdit_theme_color_font_color_selected>`               | ``Color( 0, 0, 0, 1 )``            |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`font_color_uneditable<class_LineEdit_theme_color_font_color_uneditable>`           | ``Color( 0.88, 0.88, 0.88, 0.5 )`` |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Color<class_Color>`       | :ref:`selection_color<class_LineEdit_theme_color_selection_color>`                       | ``Color( 0.49, 0.49, 0.49, 1 )``   |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`int<class_int>`           | :ref:`minimum_spaces<class_LineEdit_theme_constant_minimum_spaces>`                      | ``12``                             |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Font<class_Font>`         | :ref:`font<class_LineEdit_theme_font_font>`                                              |                                    |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`Texture<class_Texture>`   | :ref:`clear<class_LineEdit_theme_icon_clear>`                                            |                                    |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`StyleBox<class_StyleBox>` | :ref:`focus<class_LineEdit_theme_style_focus>`                                           |                                    |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`StyleBox<class_StyleBox>` | :ref:`normal<class_LineEdit_theme_style_normal>`                                         |                                    |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+
| :ref:`StyleBox<class_StyleBox>` | :ref:`read_only<class_LineEdit_theme_style_read_only>`                                   |                                    |
+---------------------------------+------------------------------------------------------------------------------------------+------------------------------------+

Señales
--------------

.. _class_LineEdit_signal_text_change_rejected:

- **text_change_rejected** **(** :ref:`String<class_String>` rejected_substring **)**

Emitted when appending text that overflows the :ref:`max_length<class_LineEdit_property_max_length>`. The appended text is truncated to fit :ref:`max_length<class_LineEdit_property_max_length>`, and the part that couldn't fit is passed as the ``rejected_substring`` argument.

----

.. _class_LineEdit_signal_text_changed:

- **text_changed** **(** :ref:`String<class_String>` new_text **)**

Emitido cuando el texto cambia.

----

.. _class_LineEdit_signal_text_entered:

- **text_entered** **(** :ref:`String<class_String>` new_text **)**

Emitido cuando el usuario presiona :ref:`@GlobalScope.KEY_ENTER<class_@GlobalScope_constant_KEY_ENTER>` en la ``LineEdit``.

Enumeraciones
--------------------------

.. _enum_LineEdit_Align:

.. _class_LineEdit_constant_ALIGN_LEFT:

.. _class_LineEdit_constant_ALIGN_CENTER:

.. _class_LineEdit_constant_ALIGN_RIGHT:

.. _class_LineEdit_constant_ALIGN_FILL:

enum **Align**:

- **ALIGN_LEFT** = **0** --- Alinea el texto en el lado izquierdo de la ``LineEdit``.

- **ALIGN_CENTER** = **1** --- Centra el texto en el centro de la ``LineEdit``.

- **ALIGN_RIGHT** = **2** --- Alinea el texto en el lado derecho de la ``LineEdit``.

- **ALIGN_FILL** = **3** --- Estira los espacios en blanco para que se ajusten al ancho de la ``LineEdit``.

----

.. _enum_LineEdit_MenuItems:

.. _class_LineEdit_constant_MENU_CUT:

.. _class_LineEdit_constant_MENU_COPY:

.. _class_LineEdit_constant_MENU_PASTE:

.. _class_LineEdit_constant_MENU_CLEAR:

.. _class_LineEdit_constant_MENU_SELECT_ALL:

.. _class_LineEdit_constant_MENU_UNDO:

.. _class_LineEdit_constant_MENU_REDO:

.. _class_LineEdit_constant_MENU_MAX:

enum **MenuItems**:

- **MENU_CUT** = **0** --- Corta (copia y borra) el texto seleccionado.

- **MENU_COPY** = **1** --- Copia el texto seleccionado.

- **MENU_PASTE** = **2** --- Pega el texto del portapapeles sobre el texto seleccionado (o en la posición del cursor).

Los caracteres de escape no imprimibles se eliminan automáticamente del portapapeles del sistema operativo a través del :ref:`String.strip_escapes<class_String_method_strip_escapes>`.

- **MENU_CLEAR** = **3** --- Borra todo el texto ``LineEdit``.

- **MENU_SELECT_ALL** = **4** --- Selecciona todo el texto ``LineEdit``.

- **MENU_UNDO** = **5** --- Deshace la acción anterior.

- **MENU_REDO** = **6** --- Invierte la última acción de deshacer.

- **MENU_MAX** = **7** --- Representa el tamaño del enum :ref:`MenuItems<enum_LineEdit_MenuItems>`.

Descripciones de Propiedades
--------------------------------------------------------

.. _class_LineEdit_property_align:

- :ref:`Align<enum_LineEdit_Align>` **align**

+-----------+------------------+
| *Default* | ``0``            |
+-----------+------------------+
| *Setter*  | set_align(value) |
+-----------+------------------+
| *Getter*  | get_align()      |
+-----------+------------------+

Alineación del texto como se define en el enum :ref:`Align<enum_LineEdit_Align>`.

----

.. _class_LineEdit_property_caret_blink:

- :ref:`bool<class_bool>` **caret_blink**

+-----------+---------------------------------+
| *Default* | ``false``                       |
+-----------+---------------------------------+
| *Setter*  | cursor_set_blink_enabled(value) |
+-----------+---------------------------------+
| *Getter*  | cursor_get_blink_enabled()      |
+-----------+---------------------------------+

Si ``true``, el caret (cursor visual) parpadea.

----

.. _class_LineEdit_property_caret_blink_speed:

- :ref:`float<class_float>` **caret_blink_speed**

+-----------+-------------------------------+
| *Default* | ``0.65``                      |
+-----------+-------------------------------+
| *Setter*  | cursor_set_blink_speed(value) |
+-----------+-------------------------------+
| *Getter*  | cursor_get_blink_speed()      |
+-----------+-------------------------------+

Duración (en segundos) del ciclo de parpadeo de un caret.

----

.. _class_LineEdit_property_caret_position:

- :ref:`int<class_int>` **caret_position**

+-----------+----------------------------+
| *Default* | ``0``                      |
+-----------+----------------------------+
| *Setter*  | set_cursor_position(value) |
+-----------+----------------------------+
| *Getter*  | get_cursor_position()      |
+-----------+----------------------------+

La posición del cursor dentro de la ``LineEdit``. Cuando se ajusta, el texto puede desplazarse para acomodarlo.

----

.. _class_LineEdit_property_clear_button_enabled:

- :ref:`bool<class_bool>` **clear_button_enabled**

+-----------+---------------------------------+
| *Default* | ``false``                       |
+-----------+---------------------------------+
| *Setter*  | set_clear_button_enabled(value) |
+-----------+---------------------------------+
| *Getter*  | is_clear_button_enabled()       |
+-----------+---------------------------------+

Si ``true``, el ``LineEdit`` mostrará un botón de borrado si ``text`` no está vacío, que puede utilizarse para borrar el texto rápidamente.

----

.. _class_LineEdit_property_context_menu_enabled:

- :ref:`bool<class_bool>` **context_menu_enabled**

+-----------+---------------------------------+
| *Default* | ``true``                        |
+-----------+---------------------------------+
| *Setter*  | set_context_menu_enabled(value) |
+-----------+---------------------------------+
| *Getter*  | is_context_menu_enabled()       |
+-----------+---------------------------------+

Si ``true``, el menú contextual aparecerá al hacer clic con el botón derecho del ratón.

----

.. _class_LineEdit_property_editable:

- :ref:`bool<class_bool>` **editable**

+-----------+---------------------+
| *Default* | ``true``            |
+-----------+---------------------+
| *Setter*  | set_editable(value) |
+-----------+---------------------+
| *Getter*  | is_editable()       |
+-----------+---------------------+

Si ``false``, el texto existente no puede ser modificado y no se puede añadir un nuevo texto.

----

.. _class_LineEdit_property_expand_to_text_length:

- :ref:`bool<class_bool>` **expand_to_text_length**

+-----------+----------------------------------+
| *Default* | ``false``                        |
+-----------+----------------------------------+
| *Setter*  | set_expand_to_text_length(value) |
+-----------+----------------------------------+
| *Getter*  | get_expand_to_text_length()      |
+-----------+----------------------------------+

Si ``true``, el ancho de ``LineEdit`` aumentará para permanecer más tiempo que el :ref:`text<class_LineEdit_property_text>`.\ **No** se comprimirá si el :ref:`text<class_LineEdit_property_text>` se acorta.

----

.. _class_LineEdit_property_max_length:

- :ref:`int<class_int>` **max_length**

+-----------+-----------------------+
| *Default* | ``0``                 |
+-----------+-----------------------+
| *Setter*  | set_max_length(value) |
+-----------+-----------------------+
| *Getter*  | get_max_length()      |
+-----------+-----------------------+

Maximum amount of characters that can be entered inside the ``LineEdit``. If ``0``, there is no limit.

When a limit is defined, characters that would exceed :ref:`max_length<class_LineEdit_property_max_length>` are truncated. This happens both for existing :ref:`text<class_LineEdit_property_text>` contents when setting the max length, or for new text inserted in the ``LineEdit``, including pasting. If any input text is truncated, the :ref:`text_change_rejected<class_LineEdit_signal_text_change_rejected>` signal is emitted with the truncated substring as parameter.

\ **Example:**\ 

::

    text = "Hello world"
    max_length = 5
    # `text` becomes "Hello".
    max_length = 10
    text += " goodbye"
    # `text` becomes "Hello good".
    # `text_change_rejected` is emitted with "bye" as parameter.

----

.. _class_LineEdit_property_placeholder_alpha:

- :ref:`float<class_float>` **placeholder_alpha**

+-----------+------------------------------+
| *Default* | ``0.6``                      |
+-----------+------------------------------+
| *Setter*  | set_placeholder_alpha(value) |
+-----------+------------------------------+
| *Getter*  | get_placeholder_alpha()      |
+-----------+------------------------------+

Opacidad del :ref:`placeholder_text<class_LineEdit_property_placeholder_text>`. De ``0`` a ``1``.

----

.. _class_LineEdit_property_placeholder_text:

- :ref:`String<class_String>` **placeholder_text**

+-----------+------------------------+
| *Default* | ``""``                 |
+-----------+------------------------+
| *Setter*  | set_placeholder(value) |
+-----------+------------------------+
| *Getter*  | get_placeholder()      |
+-----------+------------------------+

El texto se muestra cuando la ``LineEdit`` está vacía. Es **no** el valor por defecto de ``LineEdit`` (véase el :ref:`text<class_LineEdit_property_text>`).

----

.. _class_LineEdit_property_right_icon:

- :ref:`Texture<class_Texture>` **right_icon**

+----------+-----------------------+
| *Setter* | set_right_icon(value) |
+----------+-----------------------+
| *Getter* | get_right_icon()      |
+----------+-----------------------+

Establece el icono que aparecerá en el extremo derecho de la ``LineEdit`` si no hay :ref:`text<class_LineEdit_property_text>`, o siempre, si :ref:`clear_button_enabled<class_LineEdit_property_clear_button_enabled>` está establecido en ``false``.

----

.. _class_LineEdit_property_secret:

- :ref:`bool<class_bool>` **secret**

+-----------+-------------------+
| *Default* | ``false``         |
+-----------+-------------------+
| *Setter*  | set_secret(value) |
+-----------+-------------------+
| *Getter*  | is_secret()       |
+-----------+-------------------+

Si ``true``, cada carácter se sustituye por el carácter secreto (véase :ref:`secret_character<class_LineEdit_property_secret_character>`).

----

.. _class_LineEdit_property_secret_character:

- :ref:`String<class_String>` **secret_character**

+-----------+-----------------------------+
| *Default* | ``"*"``                     |
+-----------+-----------------------------+
| *Setter*  | set_secret_character(value) |
+-----------+-----------------------------+
| *Getter*  | get_secret_character()      |
+-----------+-----------------------------+

El carácter que se usará para enmascarar la entrada secreta (por defecto es "\*"). Sólo se puede utilizar un único carácter como el carácter secreto.

----

.. _class_LineEdit_property_selecting_enabled:

- :ref:`bool<class_bool>` **selecting_enabled**

+-----------+------------------------------+
| *Default* | ``true``                     |
+-----------+------------------------------+
| *Setter*  | set_selecting_enabled(value) |
+-----------+------------------------------+
| *Getter*  | is_selecting_enabled()       |
+-----------+------------------------------+

Si ``false``, es imposible seleccionar el texto usando el ratón o el teclado.

----

.. _class_LineEdit_property_shortcut_keys_enabled:

- :ref:`bool<class_bool>` **shortcut_keys_enabled**

+-----------+----------------------------------+
| *Default* | ``true``                         |
+-----------+----------------------------------+
| *Setter*  | set_shortcut_keys_enabled(value) |
+-----------+----------------------------------+
| *Getter*  | is_shortcut_keys_enabled()       |
+-----------+----------------------------------+

Si ``false``, el uso de atajos se desactivará.

----

.. _class_LineEdit_property_text:

- :ref:`String<class_String>` **text**

+-----------+-----------------+
| *Default* | ``""``          |
+-----------+-----------------+
| *Setter*  | set_text(value) |
+-----------+-----------------+
| *Getter*  | get_text()      |
+-----------+-----------------+

Valor de la strting de la ``LineEdit``.

\ **Nota:** Cambiar el texto usando esta propiedad no emitirá la señal :ref:`text_changed<class_LineEdit_signal_text_changed>`.

----

.. _class_LineEdit_property_virtual_keyboard_enabled:

- :ref:`bool<class_bool>` **virtual_keyboard_enabled**

+-----------+-------------------------------------+
| *Default* | ``true``                            |
+-----------+-------------------------------------+
| *Setter*  | set_virtual_keyboard_enabled(value) |
+-----------+-------------------------------------+
| *Getter*  | is_virtual_keyboard_enabled()       |
+-----------+-------------------------------------+

Si ``true``, el teclado virtual nativo se muestra cuando se enfoca en plataformas que lo soportan.

Descripciones de Métodos
------------------------------------------------

.. _class_LineEdit_method_append_at_cursor:

- void **append_at_cursor** **(** :ref:`String<class_String>` text **)**

Añade ``text`` después del cursor. Si el valor resultante es mayor que :ref:`max_length<class_LineEdit_property_max_length>`, no pasa nada.

----

.. _class_LineEdit_method_clear:

- void **clear** **(** **)**

Borra el :ref:`text<class_LineEdit_property_text>` de ``LineEdit``.

----

.. _class_LineEdit_method_delete_char_at_cursor:

- void **delete_char_at_cursor** **(** **)**

Deletes one character at the cursor's current position (equivalent to pressing the ``Delete`` key).

----

.. _class_LineEdit_method_delete_text:

- void **delete_text** **(** :ref:`int<class_int>` from_column, :ref:`int<class_int>` to_column **)**

Elimina una sección del :ref:`text<class_LineEdit_property_text>` que va de la posición ``from_column`` a ``to_column``. Ambos parámetros deben estar dentro de la longitud del texto.

----

.. _class_LineEdit_method_deselect:

- void **deselect** **(** **)**

Borra la selección actual.

----

.. _class_LineEdit_method_get_menu:

- :ref:`PopupMenu<class_PopupMenu>` **get_menu** **(** **)** |const|

Returns the :ref:`PopupMenu<class_PopupMenu>` of this ``LineEdit``. By default, this menu is displayed when right-clicking on the ``LineEdit``.

\ **Warning:** This is a required internal node, removing and freeing it may cause a crash. If you wish to hide it or any of its children, use their :ref:`CanvasItem.visible<class_CanvasItem_property_visible>` property.

----

.. _class_LineEdit_method_get_scroll_offset:

- :ref:`int<class_int>` **get_scroll_offset** **(** **)** |const|

Returns the scroll offset due to :ref:`caret_position<class_LineEdit_property_caret_position>`, as a number of characters.

----

.. _class_LineEdit_method_menu_option:

- void **menu_option** **(** :ref:`int<class_int>` option **)**

Ejecuta una acción determinada según se define en el enum :ref:`MenuItems<enum_LineEdit_MenuItems>`.

----

.. _class_LineEdit_method_select:

- void **select** **(** :ref:`int<class_int>` from=0, :ref:`int<class_int>` to=-1 **)**

Selecciona los caracteres dentro de ``LineEdit`` entre ``from`` y ``to``. Por defecto, ``from`` está al principio y ``to`` al final.

::

    text = "Bienvenido"
    select() # Seleccionará "Bienvenido".
    select(4) # Seleccionará "venido".
    select(2, 5) # Seleccionará "env".

----

.. _class_LineEdit_method_select_all:

- void **select_all** **(** **)**

Selecciona toda la :ref:`String<class_String>`.

Theme Property Descriptions
---------------------------

.. _class_LineEdit_theme_color_clear_button_color:

- :ref:`Color<class_Color>` **clear_button_color**

+-----------+----------------------------------+
| *Default* | ``Color( 0.88, 0.88, 0.88, 1 )`` |
+-----------+----------------------------------+

Color utilizado como tinte predeterminado para el botón de despejar.

----

.. _class_LineEdit_theme_color_clear_button_color_pressed:

- :ref:`Color<class_Color>` **clear_button_color_pressed**

+-----------+-------------------------+
| *Default* | ``Color( 1, 1, 1, 1 )`` |
+-----------+-------------------------+

Color usado para el botón de borrado cuando se presiona.

----

.. _class_LineEdit_theme_color_cursor_color:

- :ref:`Color<class_Color>` **cursor_color**

+-----------+----------------------------------+
| *Default* | ``Color( 0.94, 0.94, 0.94, 1 )`` |
+-----------+----------------------------------+

Color del cursor visual (caret) de la ``LineEdit``.

----

.. _class_LineEdit_theme_color_font_color:

- :ref:`Color<class_Color>` **font_color**

+-----------+----------------------------------+
| *Default* | ``Color( 0.88, 0.88, 0.88, 1 )`` |
+-----------+----------------------------------+

Color de fuente predeterminado.

----

.. _class_LineEdit_theme_color_font_color_selected:

- :ref:`Color<class_Color>` **font_color_selected**

+-----------+-------------------------+
| *Default* | ``Color( 0, 0, 0, 1 )`` |
+-----------+-------------------------+

Color de fuente para el texto seleccionado (dentro del rectángulo de selección).

----

.. _class_LineEdit_theme_color_font_color_uneditable:

- :ref:`Color<class_Color>` **font_color_uneditable**

+-----------+------------------------------------+
| *Default* | ``Color( 0.88, 0.88, 0.88, 0.5 )`` |
+-----------+------------------------------------+

El color de la fuente cuando la edición está desactivada.

----

.. _class_LineEdit_theme_color_selection_color:

- :ref:`Color<class_Color>` **selection_color**

+-----------+----------------------------------+
| *Default* | ``Color( 0.49, 0.49, 0.49, 1 )`` |
+-----------+----------------------------------+

Color del rectángulo de selección.

----

.. _class_LineEdit_theme_constant_minimum_spaces:

- :ref:`int<class_int>` **minimum_spaces**

+-----------+--------+
| *Default* | ``12`` |
+-----------+--------+

Espacio horizontal mínimo para el texto (sin contar el botón de borrar y los márgenes de contenido). Este valor se mide en el recuento de caracteres de espacio (es decir, esta cantidad de caracteres de espacio pueden ser mostrados sin desplazamiento).

----

.. _class_LineEdit_theme_font_font:

- :ref:`Font<class_Font>` **font**

Fuente usada para el texto.

----

.. _class_LineEdit_theme_icon_clear:

- :ref:`Texture<class_Texture>` **clear**

La textura para el botón de despejar. Ver :ref:`clear_button_enabled<class_LineEdit_property_clear_button_enabled>`.

----

.. _class_LineEdit_theme_style_focus:

- :ref:`StyleBox<class_StyleBox>` **focus**

Fondo utilizado cuando ``LineEdit`` tiene el enfoque de la interfaz gráfica de usuario(GUI).

----

.. _class_LineEdit_theme_style_normal:

- :ref:`StyleBox<class_StyleBox>` **normal**

Fondo predeterminado para la ``LineEdit``.

----

.. _class_LineEdit_theme_style_read_only:

- :ref:`StyleBox<class_StyleBox>` **read_only**

Fondo utilizado cuando ``LineEdit`` está en modo de sólo lectura (:ref:`editable<class_LineEdit_property_editable>` está configurado como ``false``).

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
