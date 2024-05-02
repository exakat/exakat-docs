.. _functions-wrongnumberofarguments:

.. _wrong-number-of-arguments:

Wrong Number Of Arguments
+++++++++++++++++++++++++

  Those functioncalls are made with too many or too few arguments. 

When the number arguments is wrong for native functions, PHP emits a warning. 
When the number arguments is too small for custom functions, PHP raises an `exception <https://www.php.net/exception>`_. 
When the number arguments is too high for custom functions, PHP ignores the arguments. Such arguments should be handled with the variadic operator, or with `func_get_args() <https://www.php.net/func_get_args>`_ family of functions.
It is recommended to check the signature of the methods, and fix the arguments.

.. code-block:: php
   
   <?php
   
   echo strtoupper('This function is', 'ignoring arguments');
   //Warning: strtoupper() expects exactly 1 parameter, 2 given in Command line code on line 1
   
   echo strtoupper();
   //Warning: strtoupper() expects exactly 1 parameter, 0 given in Command line code on line 1
   
   function foo($argument) {}
   echo foo();
   //Fatal error: Uncaught ArgumentCountError: Too few arguments to function foo(), 0 passed in /Users/famille/Desktop/analyzeG3/test.php on line 10 and exactly 1 expected in /Users/famille/Desktop/analyzeG3/test.php:3
   
   echo foo('This function is', 'ignoring arguments');
   
   ?>

Suggestions
___________

* Add more arguments to fill the list of compulsory arguments
* Remove arguments to fit the list of compulsory arguments
* Use another method or class




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongNumberOfArguments                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`IsExt <ruleset-IsExt>`, :ref:`IsPHP <ruleset-IsPHP>`, :ref:`IsStub <ruleset-IsStub>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | function, method, static-method, constructor                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-missing-argument.md <https://github.com/dseguy/clearPHP/tree/master/rules/no-missing-argument.md.md>`__                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-functions-wrongnumberofarguments`                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


