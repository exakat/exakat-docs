.. _php-php81newfunctions:


.. _new-functions-in-php-8.1:

New Functions In PHP 8.1
++++++++++++++++++++++++

.. meta::
	:description:
		New Functions In PHP 8.1: New functions are added to new PHP version.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Functions In PHP 8.1
	:twitter:description: New Functions In PHP 8.1: New functions are added to new PHP version
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Functions In PHP 8.1
	:og:type: article
	:og:description: New functions are added to new PHP version
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/New Functions In PHP 8.1.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81NewFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81NewFunctions.html","name":"New Functions In PHP 8.1","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"New functions are added to new PHP version","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/New Functions In PHP 8.1.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

New functions are added to new PHP version.

The following functions are now native functions in PHP 8.1. It is compulsory to rename any custom function that was created in older versions. One alternative is to move the function to a custom namespace, and update the use list at the beginning of the script. 

* `array_is_list() <https://www.php.net/array_is_list>`_
* `enum_exists() <https://www.php.net/enum_exists>`_
* `fsync() <https://www.php.net/fsync>`_
* `fdatasync() <https://www.php.net/fdatasync>`_
* `imagecreatefromavif() <https://www.php.net/imagecreatefromavif>`_
* `imageavif() <https://www.php.net/imageavif>`_
* `mysqli_fetch_column() <https://www.php.net/mysqli_fetch_column>`_
* `sodium_crypto_core_ristretto255_add() <https://www.php.net/sodium_crypto_core_ristretto255_add>`_
* `sodium_crypto_core_ristretto255_from_hash() <https://www.php.net/sodium_crypto_core_ristretto255_from_hash>`_
* `sodium_crypto_core_ristretto255_is_valid_point() <https://www.php.net/sodium_crypto_core_ristretto255_is_valid_point>`_
* `sodium_crypto_core_ristretto255_random() <https://www.php.net/sodium_crypto_core_ristretto255_random>`_
* `sodium_crypto_core_ristretto255_scalar_add() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_add>`_
* `sodium_crypto_core_ristretto255_scalar_complement() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_complement>`_
* `sodium_crypto_core_ristretto255_scalar_invert() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_invert>`_
* `sodium_crypto_core_ristretto255_scalar_mul() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_mul>`_
* `sodium_crypto_core_ristretto255_scalar_negate() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_negate>`_
* `sodium_crypto_core_ristretto255_scalar_random() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_random>`_
* `sodium_crypto_core_ristretto255_scalar_reduce() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_reduce>`_
* `sodium_crypto_core_ristretto255_scalar_sub() <https://www.php.net/sodium_crypto_core_ristretto255_scalar_sub>`_
* `sodium_crypto_core_ristretto255_sub() <https://www.php.net/sodium_crypto_core_ristretto255_sub>`_
* `sodium_crypto_scalarmult_ristretto255() <https://www.php.net/sodium_crypto_scalarmult_ristretto255>`_
* `sodium_crypto_scalarmult_ristretto255_base() <https://www.php.net/sodium_crypto_scalarmult_ristretto255_base>`_
* `sodium_crypto_stream_xchacha20() <https://www.php.net/sodium_crypto_stream_xchacha20>`_
* `sodium_crypto_stream_xchacha20_keygen() <https://www.php.net/sodium_crypto_stream_xchacha20_keygen>`_
* `sodium_crypto_stream_xchacha20_xor() <https://www.php.net/sodium_crypto_stream_xchacha20_xor>`_




.. code-block:: php
   
   <?php
   
   $array = [1,2,3];
   var_dump(array_is_list($array)); // true
   
   ?>
Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `Native <https://php-dictionary.readthedocs.io/en/latest/dictionary/native.ini.html>`_


Suggestions
___________

* Move custom functions with the same name to a new namespace
* Change the name of any custom functions with the same name
* Add a condition to the functions definition to avoid conflict




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81NewFunctions                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


