.. _variables-undefinedvariable:

.. _undefined-variable:

Undefined Variable
++++++++++++++++++

  Variable that is used before any initialisation. 

It is recommended to use a default value for every variable used. When not specified, the default value is set to ``NULL`` by PHP.

Variable may be created in various ways : assignation, arguments, foreach blind variables, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global variables.

This analysis doesn't handle dynamic variables, such as ``$$x``. It also doesn't handle variables outside a method or function.

.. code-block:: php
   
   <?php
   
   // Adapted from the PHP manual
   $var = 'Bob';
   $Var = 'Joe';
   // The following line may emit a warning : Undefined variable: $undefined
   echo "$var, $Var, $undefined";      // outputs "Bob, Joe, " 
   
   
   ?>

See also `Variable basics <https://www.php.net/manual/en/language.variables.basics.php>`_.


Suggestions
___________

* Remove the expression that is using the undefined variable
* Fix the variable name
* Define the variable by assigning a value to it, before using it




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UndefinedVariable                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | variable                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


