.. _performances-arraykeyexistsspeedup:

.. _array\_key\_exists()-speedup:

array_key_exists() Speedup
++++++++++++++++++++++++++

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


