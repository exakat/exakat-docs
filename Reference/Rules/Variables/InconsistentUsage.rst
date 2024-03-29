.. _variables-inconsistentusage:

.. _inconsistent-variable-usage:

Inconsistent Variable Usage
+++++++++++++++++++++++++++

  Those variables are used in various and inconsistent ways. It is difficult to understand if they are an array, an object or a scalar variable.

.. code-block:: php
   
   <?php
   
   // $a is an array, then $b is a string.
   $a = ['a', 'b', 'c'];
   $b = implode('-', $a);
   
   // $a is an array, then it is a string.
   $a = ['a', 'b', 'c'];
   $a = implode('-', $a);
   
   ?>

Suggestions
___________

* Keep one type for each variable. This keeps the code readable. 
* Give different names to variables with different types.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/InconsistentUsage                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-variables-inconsistentusage`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


