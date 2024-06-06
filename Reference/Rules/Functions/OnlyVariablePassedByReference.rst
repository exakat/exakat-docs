.. _functions-onlyvariablepassedbyreference:

.. _only-variable-passed-by-reference:

Only Variable Passed By Reference
+++++++++++++++++++++++++++++++++

  When an argument is expected by reference, it is compulsory to provide a container. A container may be a variable, an array, a property or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property. 

This may be linted by PHP, when the function definition is in the same file as the function usage. This is silently linted if definition and usage are separated, if the call is dynamical or made as a method.
This analysis currently covers functioncalls and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methodcalls, but omits methodcalls.

.. code-block:: php
   
   <?php
   
   function foo(&$bar) { /**/ }
   
   function &bar() { /**/ }
   
   // This is not possible : strtolower() returns a value
   foo(strtolower($string));
   
   // This is valid : bar() returns a reference
   foo(bar($string));
   
   ?>

See also `Passing arguments by reference <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.by-reference>`_.


Suggestions
___________

* Store the previous result in a variable, and then call the function.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/OnlyVariablePassedByReference                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | reference, parameter                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-functions-onlyvariablepassedbyreference`, :ref:`case-phpipam-functions-onlyvariablepassedbyreference` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


