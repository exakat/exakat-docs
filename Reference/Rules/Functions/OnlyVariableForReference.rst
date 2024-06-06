.. _functions-onlyvariableforreference:

.. _only-variable-for-reference:

Only Variable For Reference
+++++++++++++++++++++++++++

  When a method is requesting an argument to be a reference, it cannot be called with a literal value.

The call must be made with a variable, or any assimilated data container : array, property or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property. 
Note that PHP may detect this `error <https://www.php.net/error>`_ at linting time, if the method is defined after being called : at that point, PHP will only check the problem during execution. This is definitely the case for methods, compared to functions or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods.

.. code-block:: php
   
   <?php
   
   // This is not possible
   foo(1,2);
   
   // This is working
   foo($a, $b);
   
   function foo($a, &$b) {}
   
   ?>

See also `Passing arguments by reference <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.by-reference>`_.


Suggestions
___________

* Put the literal value in a variable before calling the method.
* Omit the arguments, when it won't be used.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/OnlyVariableForReference                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.6                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | variable, reference                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


