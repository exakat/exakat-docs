.. _structures-unsupportedtypeswithoperators:

.. _unsupported-types-with-operators:

Unsupported Types With Operators
++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Unsupported Types With Operators: Arrays, resources and objects are generally not accepted with unary and binary operators.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unsupported Types With Operators
	:twitter:description: Unsupported Types With Operators: Arrays, resources and objects are generally not accepted with unary and binary operators
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unsupported Types With Operators
	:og:type: article
	:og:description: Arrays, resources and objects are generally not accepted with unary and binary operators
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UnsupportedTypesWithOperators.html
	:og:locale: en
  Arrays, resources and objects are generally not accepted with unary and binary operators. 

The operators are `+`, `-`, `*`, `/`, `**`, `%`, `<<`, `>>`, `&`, `|`, `^`, `~`, `++` and `--`.
In PHP 8.0, the rules have been made stricter and more consistent. 

The only valid operator is `+`, combined with arrays in both operands. Other situations throw ``TypeError``.

.. code-block:: php
   
   <?php
   
   var_dump([] % [42]);
   // int(0) in PHP 7.x
   // TypeError in PHP 8.0 + 
   
   // Also impossible usage : index are string or int
   $a = [];
   $b = $c[$a]; 
   
   ?>

See also `Stricter type checks for arithmetic/bitwise operators <https://wiki.php.net/rfc/arithmetic_operator_type_checks>`_ and `TypeError <https://www.php.net/manual/en/class.typeerror.php>`_.

Related PHP errors 
-------------------

  + `Unsupported operand types <https://php-errors.readthedocs.io/en/latest/messages/unsupported-operand-types.html>`_
  + `Cannot perform bitwise not on array <https://php-errors.readthedocs.io/en/latest/messages/cannot-perform-bitwise-not-on-%25s.html>`_
  + `Cannot perform bitwise not on bool <https://php-errors.readthedocs.io/en/latest/messages/cannot-perform-bitwise-not-on-%25s.html>`_
  + `Cannot perform bitwise not on resource <https://php-errors.readthedocs.io/en/latest/messages/cannot-perform-bitwise-not-on-%25s.html>`_
  + `Cannot perform bitwise not on object <https://php-errors.readthedocs.io/en/latest/messages/cannot-perform-bitwise-not-on-%25s.html>`_



Connex PHP features
-------------------

  + `operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/operator.ini.html>`_


Suggestions
___________

* Do not use those values with those operators
* Use a condition to skip this awkward situation
* Add an extra step to turn this value into a valid type




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnsupportedTypesWithOperators                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


