.. _extensions-extlibsodium:

.. _ext-libsodium:

ext/libsodium
+++++++++++++

.. meta::
	:description:
		ext/libsodium: Extension for libsodium : in PECL until PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/libsodium
	:twitter:description: ext/libsodium: Extension for libsodium : in PECL until PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/libsodium
	:og:type: article
	:og:description: Extension for libsodium : in PECL until PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/libsodium.html
	:og:locale: en
Extension for libsodium : in PECL until PHP 7.2, and in core ever since. 

The Sodium crypto library (libsodium) is a modern, easy-to-use software library for encryption, decryption, signatures, password hashing and more.

Sodium supports a variety of compilers and operating systems, including Windows (with MinGW or Visual Studio, x86 and x64), iOS and Android.

The design choices emphasize security, and "magic constants" have clear rationales.

.. code-block:: php
   
   <?php
   // Example from the docs : https://paragonie.com/book/pecl-libsodium/read/06-hashing.md#crypto-generichash
   
   // Fast, unkeyed hash function.
   // Can be used as a secure replacement for MD5
   $h = \Sodium\crypto_generichash('msg');
   
   // Fast, keyed hash function.
   // The key can be of any length between \Sodium\CRYPTO_GENERICHASH_KEYBYTES_MIN
   // and \Sodium\CRYPTO_GENERICHASH_KEYBYTES_MAX, in bytes.
   // \Sodium\CRYPTO_GENERICHASH_KEYBYTES is the recommended length.
   $h = \Sodium\crypto_generichash('msg', $key);
   
   // Fast, keyed hash function, with user-chosen output length, in bytes.
   // Output length can be between \Sodium\CRYPTO_GENERICHASH_BYTES_MIN and
   // \Sodium\CRYPTO_GENERICHASH_BYTES_MAX.
   // \Sodium\CRYPTO_GENERICHASH_BYTES is the default length.
   $h = \Sodium\crypto_generichash('msg', $key, 64);
   
   ?>

See also `PHP extension for libsodium <https://github.com/jedisct1/libsodium-php>`_ and `Using Libsodium in PHP Projects <https://paragonie.com/book/pecl-libsodium/read/00-intro.md>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extlibsodium                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.2                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


