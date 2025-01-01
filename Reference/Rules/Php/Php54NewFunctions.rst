.. _php-php54newfunctions:

.. _new-functions-in-php-5.4:

New Functions In PHP 5.4
++++++++++++++++++++++++

.. meta::
	:description:
		New Functions In PHP 5.4: PHP introduced new functions in PHP 5.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Functions In PHP 5.4
	:twitter:description: New Functions In PHP 5.4: PHP introduced new functions in PHP 5
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Functions In PHP 5.4
	:og:type: article
	:og:description: PHP introduced new functions in PHP 5
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php54NewFunctions.html
	:og:locale: en
PHP introduced new functions in PHP 5.4. If there are defined functions with such names, there will be a conflict when upgrading. It is advised to change those functions' name.

+ `hex2bin() <https://www.php.net/hex2bin>`_
+ `http_response_code() <https://www.php.net/http_response_code>`_
+ `get_declared_traits() <https://www.php.net/get_declared_traits>`_
+ `getimagesizefromstring() <https://www.php.net/getimagesizefromstring>`_
+ `stream_set_chunk_size() <https://www.php.net/stream_set_chunk_size>`_
+ `socket_import_stream() <https://www.php.net/socket_import_stream>`_
+ `trait_exists() <https://www.php.net/trait_exists>`_
+ `header_register_callback() <https://www.php.net/header_register_callback>`_
+ `class_uses() <https://www.php.net/class_uses>`_
+ `session_status() <https://www.php.net/session_status>`_
+ `session_register_shutdown() <https://www.php.net/session_register_shutdown>`_
+ `mysqli_error_list() <https://www.php.net/mysqli_error_list>`_
+ `mysqli_stmt_error_list() <https://www.php.net/mysqli_stmt_error_list>`_
+ `libxml_set_external_entity_loader() <https://www.php.net/libxml_set_external_entity_loader>`_
+ ldap_control_paged_result()
+ ldap_control_paged_result_response()
+ `transliterator_create() <https://www.php.net/transliterator_create>`_
+ `transliterator_create_from_rules() <https://www.php.net/transliterator_create_from_rules>`_
+ `transliterator_create_inverse() <https://www.php.net/transliterator_create_inverse>`_
+ `transliterator_get_error_code() <https://www.php.net/transliterator_get_error_code>`_
+ `transliterator_get_error_message() <https://www.php.net/transliterator_get_error_message>`_
+ `transliterator_list_ids() <https://www.php.net/transliterator_list_ids>`_
+ `transliterator_transliterate() <https://www.php.net/transliterator_transliterate>`_
+ `zlib_decode() <https://www.php.net/zlib_decode>`_
+ `zlib_encode() <https://www.php.net/zlib_encode>`_

.. code-block:: php
   
   <?php
   
   $zipped = zlib_encode($longText); 
   
   $raw = zlib_decode($zipped);
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php54NewFunctions                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.3 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


