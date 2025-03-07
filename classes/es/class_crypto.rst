:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the Crypto.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_Crypto:

Crypto
======

**Inherits:** :ref:`Reference<class_Reference>` **<** :ref:`Object<class_Object>`

Acceso a funcionalidades criptográficas avanzadas.

Descripción
----------------------

La clase Criptográfica le permite acceder a algunas funcionalidades criptográficas más avanzadas en Godot.

Por ahora, esto incluye la generación de bytes aleatorios criptográficamente seguros, claves RSA y generación de certificados X509 autofirmados, encriptación/desencriptación de claves asimétricas y firma/verificación.

::

    extends Node
    
    var crypto = Crypto.new()
    var clave = CryptoKey.new()
    var certificado = X509Certificate.new()
    
    func _ready():
        # Genera una clave nueva RSA.
        clave = crypto.generate_rsa(4096)
        # Genera un certificado autofirmado con la clave dada.
        certificado = crypto.generate_self_signed_certificate(clave, "CN=mydomain.com,O=My Game Company,C=IT")
        # Guarda la clave y el certificado en un directorio del usuario.
        clave.save("user://generada.key")
        certificado.save("user://generada.crt")
        # Encripción
        var datos = "Algunos datos"
        var encriptado = crypto.encrypt(clave, datos.to_utf8())
        # Desencriptado
        var desencriptado = crypto.decrypt(clave, encriptado)
        # Firmada
        var firma = crypto.sign(HashingContext.HASH_SHA256, datos.sha256_buffer(), clave)
        # Verificar
        var verificado = crypto.verify(HashingContext.HASH_SHA256, datos.sha256_buffer(), firma, clave)
        # Cheque
        assert(verificado)
        assert(datos.to_utf8() == desencriptado)

\ **Nota:** No disponible en los exportables HTML5.

Métodos
--------------

+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                       | :ref:`constant_time_compare<class_Crypto_method_constant_time_compare>` **(** :ref:`PoolByteArray<class_PoolByteArray>` trusted, :ref:`PoolByteArray<class_PoolByteArray>` received **)**                                                                                                                                                     |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolByteArray<class_PoolByteArray>`     | :ref:`decrypt<class_Crypto_method_decrypt>` **(** :ref:`CryptoKey<class_CryptoKey>` key, :ref:`PoolByteArray<class_PoolByteArray>` ciphertext **)**                                                                                                                                                                                           |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolByteArray<class_PoolByteArray>`     | :ref:`encrypt<class_Crypto_method_encrypt>` **(** :ref:`CryptoKey<class_CryptoKey>` key, :ref:`PoolByteArray<class_PoolByteArray>` plaintext **)**                                                                                                                                                                                            |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolByteArray<class_PoolByteArray>`     | :ref:`generate_random_bytes<class_Crypto_method_generate_random_bytes>` **(** :ref:`int<class_int>` size **)**                                                                                                                                                                                                                                |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`CryptoKey<class_CryptoKey>`             | :ref:`generate_rsa<class_Crypto_method_generate_rsa>` **(** :ref:`int<class_int>` size **)**                                                                                                                                                                                                                                                  |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`X509Certificate<class_X509Certificate>` | :ref:`generate_self_signed_certificate<class_Crypto_method_generate_self_signed_certificate>` **(** :ref:`CryptoKey<class_CryptoKey>` key, :ref:`String<class_String>` issuer_name="CN=myserver,O=myorganisation,C=IT", :ref:`String<class_String>` not_before="20140101000000", :ref:`String<class_String>` not_after="20340101000000" **)** |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolByteArray<class_PoolByteArray>`     | :ref:`hmac_digest<class_Crypto_method_hmac_digest>` **(** :ref:`HashType<enum_HashingContext_HashType>` hash_type, :ref:`PoolByteArray<class_PoolByteArray>` key, :ref:`PoolByteArray<class_PoolByteArray>` msg **)**                                                                                                                         |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolByteArray<class_PoolByteArray>`     | :ref:`sign<class_Crypto_method_sign>` **(** :ref:`HashType<enum_HashingContext_HashType>` hash_type, :ref:`PoolByteArray<class_PoolByteArray>` hash, :ref:`CryptoKey<class_CryptoKey>` key **)**                                                                                                                                              |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                       | :ref:`verify<class_Crypto_method_verify>` **(** :ref:`HashType<enum_HashingContext_HashType>` hash_type, :ref:`PoolByteArray<class_PoolByteArray>` hash, :ref:`PoolByteArray<class_PoolByteArray>` signature, :ref:`CryptoKey<class_CryptoKey>` key **)**                                                                                     |
+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Descripciones de Métodos
------------------------------------------------

.. _class_Crypto_method_constant_time_compare:

- :ref:`bool<class_bool>` **constant_time_compare** **(** :ref:`PoolByteArray<class_PoolByteArray>` trusted, :ref:`PoolByteArray<class_PoolByteArray>` received **)**

Compares two :ref:`PoolByteArray<class_PoolByteArray>`\ s for equality without leaking timing information in order to prevent timing attacks.

See `this blog post <https://paragonie.com/blog/2015/11/preventing-timing-attacks-on-string-comparison-with-double-hmac-strategy>`__ for more information.

----

.. _class_Crypto_method_decrypt:

- :ref:`PoolByteArray<class_PoolByteArray>` **decrypt** **(** :ref:`CryptoKey<class_CryptoKey>` key, :ref:`PoolByteArray<class_PoolByteArray>` ciphertext **)**

Decrypt the given ``ciphertext`` with the provided private ``key``.

\ **Note:** The maximum size of accepted ciphertext is limited by the key size.

----

.. _class_Crypto_method_encrypt:

- :ref:`PoolByteArray<class_PoolByteArray>` **encrypt** **(** :ref:`CryptoKey<class_CryptoKey>` key, :ref:`PoolByteArray<class_PoolByteArray>` plaintext **)**

Encrypt the given ``plaintext`` with the provided public ``key``.

\ **Note:** The maximum size of accepted plaintext is limited by the key size.

----

.. _class_Crypto_method_generate_random_bytes:

- :ref:`PoolByteArray<class_PoolByteArray>` **generate_random_bytes** **(** :ref:`int<class_int>` size **)**

Generates a :ref:`PoolByteArray<class_PoolByteArray>` of cryptographically secure random bytes with given ``size``.

----

.. _class_Crypto_method_generate_rsa:

- :ref:`CryptoKey<class_CryptoKey>` **generate_rsa** **(** :ref:`int<class_int>` size **)**

Genera una RSA :ref:`CryptoKey<class_CryptoKey>` que puede ser utilizada para crear certificados autofirmados y pasarla a :ref:`StreamPeerSSL.accept_stream<class_StreamPeerSSL_method_accept_stream>`.

----

.. _class_Crypto_method_generate_self_signed_certificate:

- :ref:`X509Certificate<class_X509Certificate>` **generate_self_signed_certificate** **(** :ref:`CryptoKey<class_CryptoKey>` key, :ref:`String<class_String>` issuer_name="CN=myserver,O=myorganisation,C=IT", :ref:`String<class_String>` not_before="20140101000000", :ref:`String<class_String>` not_after="20340101000000" **)**

Genera un :ref:`X509Certificate<class_X509Certificate>` autofirmado a partir de la :ref:`CryptoKey<class_CryptoKey>` y el ``issuer_name`` dados. La validez del certificado se definirá mediante ``not_before`` y ``not_after`` (primera fecha de validez y última fecha de validez). El ``issuer_name`` debe contener al menos "CN=" (nombre común, es decir, el nombre del dominio), "O=" (organización, es decir, el nombre de su empresa), "C=" (país, es decir, el código ISO-3166 de dos letras del país en el que la organización tiene su sede).

Un pequeño ejemplo para generar una clave RSA y un certificado autofirmado X509.

::

    var criptografia = Crypto.new()
    # Genera una clave de 4096 bits RSA.
    var clave = criptografia.generate_rsa(4096)
    # Genera un certificado autofirmado usando la clave.
    var certificado = criptografia.generate_self_signed_certificate(key, "CN=example.com,O=A Game Company,C=IT")

----

.. _class_Crypto_method_hmac_digest:

- :ref:`PoolByteArray<class_PoolByteArray>` **hmac_digest** **(** :ref:`HashType<enum_HashingContext_HashType>` hash_type, :ref:`PoolByteArray<class_PoolByteArray>` key, :ref:`PoolByteArray<class_PoolByteArray>` msg **)**

Generates an `HMAC <https://en.wikipedia.org/wiki/HMAC>`__ digest of ``msg`` using ``key``. The ``hash_type`` parameter is the hashing algorithm that is used for the inner and outer hashes.

Currently, only :ref:`HashingContext.HASH_SHA256<class_HashingContext_constant_HASH_SHA256>` and :ref:`HashingContext.HASH_SHA1<class_HashingContext_constant_HASH_SHA1>` are supported.

----

.. _class_Crypto_method_sign:

- :ref:`PoolByteArray<class_PoolByteArray>` **sign** **(** :ref:`HashType<enum_HashingContext_HashType>` hash_type, :ref:`PoolByteArray<class_PoolByteArray>` hash, :ref:`CryptoKey<class_CryptoKey>` key **)**

Firma un ``hash`` de tipo ``hash_type`` con la ``key`` privada proporcionada.

----

.. _class_Crypto_method_verify:

- :ref:`bool<class_bool>` **verify** **(** :ref:`HashType<enum_HashingContext_HashType>` hash_type, :ref:`PoolByteArray<class_PoolByteArray>` hash, :ref:`PoolByteArray<class_PoolByteArray>` signature, :ref:`CryptoKey<class_CryptoKey>` key **)**

Verifique que un ``signature`` dado para ``hash`` de tipo ``hash_tipo`` contra el ``key`` público proporcionado.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
