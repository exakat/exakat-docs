.. _structures-catchshadowsvariable:

.. _catch-overwrite-variable:

Catch Overwrite Variable
++++++++++++++++++++++++

  The try/catch structure uses some variables that are also in use in this scope. In case of a caught `exception <https://www.php.net/exception>`_, the `exception <https://www.php.net/exception>`_ will be put in the catch variable, and overwrite the current value, loosing some data.
It is recommended to use another name for these catch variables.

.. code-block:: php
   
   <?php
   
   // variables and caught exceptions are distinct
   $argument = 1;
   try {
       methodThatMayRaiseException($argument);
   } (Exception $e) {
       // here, $e has been changed to an exception.
   }
   
   // variables and caught exceptions are overlapping
   $e = 1;
   try {
       methodThatMayRaiseException();
   } (Exception $e) {
       // here, $e has been changed to an exception.
   }
   
   ?>

Suggestions
___________

* Use a standard : only use $e (or else) to catch exceptions. Avoid using them for anything else, parameter, property or local variable.
* Change the variable, and keep the caught exception




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CatchShadowsVariable                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | try-catch                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-catch-overwrite <https://github.com/dseguy/clearPHP/tree/master/rules/no-catch-overwrite.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpipam-structures-catchshadowsvariable`, :ref:`case-suitecrm-structures-catchshadowsvariable`               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


