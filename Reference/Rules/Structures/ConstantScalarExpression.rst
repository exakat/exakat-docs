.. _structures-constantscalarexpression:

.. _constant-scalar-expressions:

Constant Scalar Expressions
+++++++++++++++++++++++++++

.. meta::
	:description:
		Constant Scalar Expressions: Define constant with the result of static expressions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Scalar Expressions
	:twitter:description: Constant Scalar Expressions: Define constant with the result of static expressions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Scalar Expressions
	:og:type: article
	:og:description: Define constant with the result of static expressions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ConstantScalarExpression.html
	:og:locale: en
Define constant with the `result <https://www.php.net/result>`_ of `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expressions. This means that constants may be defined with the const keyword, with the help of various operators but without any functioncalls. 

This feature was introduced in PHP 5.6. It also supports `array() <https://www.php.net/array>`_, and expressions in arrays.

Those expressions (using simple operators) may only manipulate other constants, and all values must be known at compile time.

.. code-block:: php
   
   <?php
   
   // simple definition
   const A = 1;
   
   // constant scalar expression
   const B = A * 3;
   
   // constant scalar expression
   const C = [A ** 3, '3' => B];
   
   ?>

See also `Constant Scalar Expressions <https://wiki.php.net/rfc/const_scalar_exprs>`_.

Connex PHP features
-------------------

  + `constant-scalar-expression <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant-scalar-expression.ini.html>`_


Specs
_____

+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/ConstantScalarExpression                                                                                                                                                                                                                                                                            |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                                                                                                          |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 5.6 and more recent                                                                                                                                                                                                                                                                                   |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                                                                                                                          |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                                                                                                                |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.6                                                                                                                                                                                                                                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                                                                                                      |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


