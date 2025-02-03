.. _performances-arraykeyexistsspeedup:


.. _array\_key\_exists()-speedup:

array_key_exists() Speedup
++++++++++++++++++++++++++


.. meta::

	:description:

		array_key_exists() Speedup: array_key_exists() has its own opcode, leading to better features and speed.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: array_key_exists() Speedup

	:twitter:description: array_key_exists() Speedup: array_key_exists() has its own opcode, leading to better features and speed

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: array_key_exists() Speedup

	:og:type: article

	:og:description: array_key_exists() has its own opcode, leading to better features and speed

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/array_key_exists() Speedup.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ArrayKeyExistsSpeedup.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ArrayKeyExistsSpeedup.html","name":"array_key_exists() Speedup","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"array_key_exists() has its own opcode, leading to better features and speed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/array_key_exists() Speedup.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_key_exists() <https://www.php.net/array_key_exists>`_ has its own opcode, leading to better features and speed.

`isset() <https://www.www.php.net/isset>`_ is faster for all non-empty values, but is limited when the value is `NULL <https://www.php.net/manual/en/language.types.null.php>`_ or empty : then, `array_key_exists() <https://www.php.net/array_key_exists>`_ has the good features.

``This change makes `array_key_exists() <https://www.php.net/array_key_exists>`_ actually faster than `isset() <https://www.www.php.net/isset>`_ by ~25% (tested with GCC 8, -O3, march=native, mtune=native).``.

.. code-block:: php
   
   <?php
   
   $foo = [123 => 456];
   
   // This is sufficient and efficient since PHP 7.4
   if (array_search_key($foo[123])) {
       // do something
   }
   
   // taking advantages of performances for PHP 7.4 and older
   if (isset($foo[123]) || array_search_key($foo[123])) {
       // do something
   }
   
   ?>

See also `Implement ZEND_ARRAY_KEY_EXISTS opcode to speed up array_key_exists() <https://github.com/php/php-src/pull/3360>`_.

Connex PHP features
-------------------

  + `opcode <https://php-dictionary.readthedocs.io/en/latest/dictionary/opcode.ini.html>`_


Suggestions
___________

* Remove the isset() call and the logical operator




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/ArrayKeyExistsSpeedup                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.1                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


