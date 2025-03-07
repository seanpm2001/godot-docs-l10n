:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the IP.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_IP:

IP
==

**Inherits:** :ref:`Object<class_Object>`

互联网协议（IP）支持功能，如DNS解析。

描述
----

IP包含对互联网协议（IP）的支持功能。TCP/IP支持在不同的类别中（见\ :ref:`StreamPeerTCP<class_StreamPeerTCP>`\ 和\ :ref:`TCP_Server<class_TCP_Server>`\ ）。IP提供DNS主机名解析支持，包括阻塞式和线程式。

方法
----

+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`clear_cache<class_IP_method_clear_cache>` **(** :ref:`String<class_String>` hostname="" **)**                                                               |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                          | :ref:`erase_resolve_item<class_IP_method_erase_resolve_item>` **(** :ref:`int<class_int>` id **)**                                                                |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`                     | :ref:`get_local_addresses<class_IP_method_get_local_addresses>` **(** **)** |const|                                                                               |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`                     | :ref:`get_local_interfaces<class_IP_method_get_local_interfaces>` **(** **)** |const|                                                                             |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`String<class_String>`                   | :ref:`get_resolve_item_address<class_IP_method_get_resolve_item_address>` **(** :ref:`int<class_int>` id **)** |const|                                            |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`                     | :ref:`get_resolve_item_addresses<class_IP_method_get_resolve_item_addresses>` **(** :ref:`int<class_int>` id **)** |const|                                        |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`ResolverStatus<enum_IP_ResolverStatus>` | :ref:`get_resolve_item_status<class_IP_method_get_resolve_item_status>` **(** :ref:`int<class_int>` id **)** |const|                                              |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`String<class_String>`                   | :ref:`resolve_hostname<class_IP_method_resolve_hostname>` **(** :ref:`String<class_String>` host, :ref:`Type<enum_IP_Type>` ip_type=3 **)**                       |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`                     | :ref:`resolve_hostname_addresses<class_IP_method_resolve_hostname_addresses>` **(** :ref:`String<class_String>` host, :ref:`Type<enum_IP_Type>` ip_type=3 **)**   |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                         | :ref:`resolve_hostname_queue_item<class_IP_method_resolve_hostname_queue_item>` **(** :ref:`String<class_String>` host, :ref:`Type<enum_IP_Type>` ip_type=3 **)** |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

枚举
----

.. _enum_IP_ResolverStatus:

.. _class_IP_constant_RESOLVER_STATUS_NONE:

.. _class_IP_constant_RESOLVER_STATUS_WAITING:

.. _class_IP_constant_RESOLVER_STATUS_DONE:

.. _class_IP_constant_RESOLVER_STATUS_ERROR:

enum **ResolverStatus**:

- **RESOLVER_STATUS_NONE** = **0** --- DNS 主机名解析器状态：无状态。

- **RESOLVER_STATUS_WAITING** = **1** --- DNS 主机名解析器状态：正在等待。

- **RESOLVER_STATUS_DONE** = **2** --- DNS 主机名解析器状态：完成。

- **RESOLVER_STATUS_ERROR** = **3** --- DNS 主机名解析器状态：错误。

----

.. _enum_IP_Type:

.. _class_IP_constant_TYPE_NONE:

.. _class_IP_constant_TYPE_IPV4:

.. _class_IP_constant_TYPE_IPV6:

.. _class_IP_constant_TYPE_ANY:

enum **Type**:

- **TYPE_NONE** = **0** --- 地址类型：无。

- **TYPE_IPV4** = **1** --- 地址类型：互联网协议版本4（IPv4）。

- **TYPE_IPV6** = **2** --- 地址类型：互联网协议版本6（IPv6）。

- **TYPE_ANY** = **3** --- 地址类型：任意。

常量
----

.. _class_IP_constant_RESOLVER_MAX_QUERIES:

.. _class_IP_constant_RESOLVER_INVALID_ID:

- **RESOLVER_MAX_QUERIES** = **32** --- 允许的最大并发DNS解析器查询数量，如果超过，则返回\ :ref:`RESOLVER_INVALID_ID<class_IP_constant_RESOLVER_INVALID_ID>`\ 。

- **RESOLVER_INVALID_ID** = **-1** --- 无效的ID常数。如果超过了\ :ref:`RESOLVER_MAX_QUERIES<class_IP_constant_RESOLVER_MAX_QUERIES>`\ ，则返回。

方法说明
--------

.. _class_IP_method_clear_cache:

- void **clear_cache** **(** :ref:`String<class_String>` hostname="" **)**

移除所有\ ``hostname``\ 主机名的缓存引用。如果没有给出\ ``hostname``\ ，所有缓存的IP地址将被删除。

----

.. _class_IP_method_erase_resolve_item:

- void **erase_resolve_item** **(** :ref:`int<class_int>` id **)**

从队列中删除一个给定的项目\ ``id``\ 。这应该被用来在队列完成后释放队列，以便进行更多的查询。

----

.. _class_IP_method_get_local_addresses:

- :ref:`Array<class_Array>` **get_local_addresses** **(** **)** |const|

以数组形式返回所有用户的当前IPv4和IPv6地址。

----

.. _class_IP_method_get_local_interfaces:

- :ref:`Array<class_Array>` **get_local_interfaces** **(** **)** |const|

以数组形式返回所有网络适配器(network adapters)。

每个适配器是一个形式的字典。

::

    {
        "index":"1", # 接口索引。
        "name":"eth0", # 接口名称。
        "friendly":"Ethernet One", # 一个友好的名字（可能是空的）。
        "address":["192.168.1.101"], # 一个与此接口相关的IP地址数组。
    }

----

.. _class_IP_method_get_resolve_item_address:

- :ref:`String<class_String>` **get_resolve_item_address** **(** :ref:`int<class_int>` id **)** |const|

给定队列 ``id``\ ，返回排队主机名的 IP 地址。出现错误或解析尚未发生时返回一个空字符串（参阅 :ref:`get_resolve_item_status<class_IP_method_get_resolve_item_status>`\ ）。

----

.. _class_IP_method_get_resolve_item_addresses:

- :ref:`Array<class_Array>` **get_resolve_item_addresses** **(** :ref:`int<class_int>` id **)** |const|

如果发生错误或尚未发生解析，则返回已解析的地址或空数组（请参阅 :ref:`get_resolve_item_status<class_IP_method_get_resolve_item_status>`\ ）。

----

.. _class_IP_method_get_resolve_item_status:

- :ref:`ResolverStatus<enum_IP_ResolverStatus>` **get_resolve_item_status** **(** :ref:`int<class_int>` id **)** |const|

给定队列 ``id``\ ，以 :ref:`ResolverStatus<enum_IP_ResolverStatus>` 常量的形式返回排队主机名的状态。

----

.. _class_IP_method_resolve_hostname:

- :ref:`String<class_String>` **resolve_hostname** **(** :ref:`String<class_String>` host, :ref:`Type<enum_IP_Type>` ip_type=3 **)**

在解析时返回一个给定的主机名的IPv4或IPv6地址（阻塞类型方法）。返回的地址类型取决于作为\ ``ip_type``\ 的\ :ref:`Type<enum_IP_Type>`\ 常量。

----

.. _class_IP_method_resolve_hostname_addresses:

- :ref:`Array<class_Array>` **resolve_hostname_addresses** **(** :ref:`String<class_String>` host, :ref:`Type<enum_IP_Type>` ip_type=3 **)**

以阻塞方式解析给定的主机名。地址作为 IPv4 或 IPv6 的 :ref:`Array<class_Array>` 数组返回，具体取决于 ``ip_type``\ 。

----

.. _class_IP_method_resolve_hostname_queue_item:

- :ref:`int<class_int>` **resolve_hostname_queue_item** **(** :ref:`String<class_String>` host, :ref:`Type<enum_IP_Type>` ip_type=3 **)**

创建一个队列项目，根据\ :ref:`Type<enum_IP_Type>`\ 常数\ ``ip_type``\ ，将主机名解析为IPv4或IPv6地址。如果成功，返回队列ID，否则返回\ :ref:`RESOLVER_INVALID_ID<class_IP_constant_RESOLVER_INVALID_ID>`\ 。

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
