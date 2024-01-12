.. _php-onlyvariablepassedbyreference:

.. _only-variable-passed-by-reference:

Only Variable Passed By Reference
+++++++++++++++++++++++++++++++++

  Some methods require a variable as argument. Those arguments are passed by reference, and they must operate on a variable, or any data container (property, array element). 

This means that literal values, constants cannot be used as argument. This is also the case of literal values, returned by other methods.

This is also the case of ``isset()``, althought with a different `error <https://www.php.net/error>`_ message.



.. code-block:: php
   
   <?php
   
   echo end([1,2,3]);
   
   function foo() {
   	return [4,5,6];
   }
   
   echo end(foo());
   
   ?>

Suggestions
___________

* Put the value in a variable before using it with the function.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------+
| Short name   | Php/OnlyVariablePassedByReference                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------+
| Available in |                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------+


