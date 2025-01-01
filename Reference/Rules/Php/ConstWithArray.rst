.. _php-constwitharray:

.. _const-with-array:

Const With Array
++++++++++++++++

.. meta::
	:description:
		Const With Array: The const keyword supports array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Const With Array
	:twitter:description: Const With Array: The const keyword supports array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Const With Array
	:og:type: article
	:og:description: The const keyword supports array
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ConstWithArray.html
	:og:locale: en
The const keyword supports array. This feature was added in PHP 5.6. 

The array must be filled with other constants. It may also be build using the '+' operator.

.. code-block:: php
   
   <?php
   
   const PRIMES = [2, 3, 5, 7];
   
   class X {
       const TWENTY_THREE = 23;
       const MORE_PRIMES = PRIMES + [11, 13, 17, 19];
       const EVEN_MORE_PRIMES = self::MORE_PRIMES + [self::TWENTY_THREE];
   }
   
   ?>

See also `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_ and `Constants Syntax <https://www.php.net/manual/en/language.constants.syntax.php>`_.

Connex PHP features
-------------------

  + `random <https://php-dictionary.readthedocs.io/en/latest/dictionary/random.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ConstWithArray                                                                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


