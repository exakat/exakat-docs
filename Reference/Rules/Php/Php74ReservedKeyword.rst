.. _php-php74reservedkeyword:

.. _php-7.4-reserved-keyword:

PHP 7.4 Reserved Keyword
++++++++++++++++++++++++

  ``fn`` is a new PHP keyword. In PHP 7.4, it is used to build the arrow functions. When used at an illegal position, ``fn`` generates a Fatal `error <https://www.php.net/error>`_ at compile time.

As a key word, ``fn`` is not allowed as constant name, function name, class name or inside namespaces. 


.. code-block:: php
   
   <?php
   
   // PHP 7.4 usage of fn
   function array_values_from_keys($arr, $keys) {
       return array_map(fn($x) => $arr[$x], $keys);
   }
   
   // PHP 7.3 usage of fn
   const fn = 1;
   
   function fn() {}
   
   class x {
       // This is valid in PHP 7.3 and 7.4
       function fn() {}
   }
   
   ?>


``fn`` is fine for method names. It may also be used for constants with `define() <https://www.php.net/define>`_, and `constant() <https://www.php.net/constant>`_ but it is not recommended.

See also `PHP RFC: Arrow Functions <https://wiki.php.net/rfc/arrow_functions>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php74ReservedKeyword                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


