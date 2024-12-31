.. _php-spreadoperatorforarray:

.. _spread-operator-for-array:

Spread Operator For Array
+++++++++++++++++++++++++

.. meta\:\:
	:description:
		Spread Operator For Array: The variadic operator may be used with arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Spread Operator For Array
	:twitter:description: Spread Operator For Array: The variadic operator may be used with arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Spread Operator For Array
	:og:type: article
	:og:description: The variadic operator may be used with arrays
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/SpreadOperatorForArray.html
	:og:locale: en
  The variadic operator may be used with arrays. This has been introduced in PHP 7.4. 

`list() <https://www.php.net/list>`_ is not allowed to use this operator, as `list() <https://www.php.net/list>`_ expected variables, not values.

.. code-block:: php
   
   <?php
   
   $array = [1, 2, 3];
   $extended_array = [...$array, 4, 5, 6];
   
   // invalid syntax
   [...$a] = [1,2,3];
   
   ?>

See also `Spread Operator in Array Expression <https://wiki.php.net/rfc/spread_operator_for_array>`_.

Connex PHP features
-------------------

  + `variadic <https://php-dictionary.readthedocs.io/en/latest/dictionary/variadic.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SpreadOperatorForArray                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


