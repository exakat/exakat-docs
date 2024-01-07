.. _structures-implicitconversiontoint:

.. _implicit-conversion-to-int:

Implicit Conversion To Int
++++++++++++++++++++++++++

  PHP warns when a value is implicitely converted from float to int. This usually leads to a loss of precision and unexpected values.

The conversion happens in various situations in PHP lifecycle (extracted from the wiki article): 

+ Bitwise OR operator |
+ Bitwise AND operator &
+ Bitwise XOR operator ^
+ Shift right and left operators
+ Modulo operator
+ The combined assignment operators of the above operators
+ Assignment to a typed property of type int in coercive typing mode
+ Argument for a parameter of type int for both internal and custom functions in coercive typing mode
+ Returning such a value for custom functions declared with a return type of int in coercive typing mode
+ Bitwise NOT operator ~
+ As an array key



This features is applied to PHP 8.1 and later, yet it is also applicable to older versions of PHP.

.. code-block:: php
   
   <?php
   
   function foo(int $i) {}
   
   //Implicit conversion from float 1.2 to int loses precision
   foo(1.2);
   
   ?>

See also `PHP RFC: Deprecate implicit non-integer-compatible float to int conversions <https://wiki.php.net/rfc/implicit-float-int-deprecate>`_.


Suggestions
___________

* Add an explicit cast `(int)` operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ImplicitConversionToInt                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | type-juggling                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


