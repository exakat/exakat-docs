.. _functions-mismatchtypeanddefault:

.. _mismatch-type-and-default:

Mismatch Type And Default
+++++++++++++++++++++++++

.. meta::
	:description:
		Mismatch Type And Default: The argument typehint and its default value don't match.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatch Type And Default
	:twitter:description: Mismatch Type And Default: The argument typehint and its default value don't match
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatch Type And Default
	:og:type: article
	:og:description: The argument typehint and its default value don't match
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mismatch Type And Default.html
	:og:locale: en
The argument typehint and its default value don't match. 

The code may lint and load, and even work when the arguments are provided. Though, PHP won't eventually execute it. 

Most of the mismatch problems are caught by PHP at linting time. It displays the following `error <https://www.php.net/error>`_ message : 'Argument 1 passed to foo() must be of the type integer, string given'.

The default value may be a constant (normal or class constant) : as such, PHP might find its value only at execution time, from another include. As such, PHP doesn't report anything about the situation at compile time.

The default value may also be a constant scalar expression : since PHP 7, some of the simple operators such as +, -, *, %, `** <https://www.php.net/manual/en/language.operators.arithmetic.php>`_, etc. are available to build default values. Among them, the ternary operator and Coalesce. Again, those expression may be only evaluated at execution time, when the value of the constants are known. 

PHP reports typehint and default mismatch at compilation time, unless there is a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expression that can't be resolved within the compiled file : then it is checked only at runtime, leading to a Fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // bad definition : the string is actually an integer
   const STRING = 3;
   
   function foo(string $s = STRING) {
       echo $s;
   }
   
   // works without problem
   foo('string');
   
   // Fatal error at compile time
   foo();
   
   // Fail only at execution time (missing D), and when default is needed
   function foo2(string $s = D ? null : array()) {
       echo $s;
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_, :ref:`Wrong Type Returned <wrong-type-returned>`, :ref:`Mismatch Type And Default <mismatch-type-and-default>` and :ref:`Wrong Typed Property Default <wrong-typed-property-default>`.

Related PHP errors 
-------------------

  + `Argument 1 passed to foo() must be of the type integer, string given <https://php-errors.readthedocs.io/en/latest/messages/argument-%23%25d-%5C%28%24%25s%5C%29-must-be-of-type-%25s%5C%2C-%25s-given.html>`_
  + `Default value for parameters with a int type can only be int or NULL <https://php-errors.readthedocs.io/en/latest/messages/default-value-for-parameters-with-a-%25s-type-can-only-be-%25s-or-null.html>`_



Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `default <https://php-dictionary.readthedocs.io/en/latest/dictionary/default.ini.html>`_


Suggestions
___________

* Match the typehint with the default value
* Do not rely on PHP type juggling to change the type on the fly




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchTypeAndDefault                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


