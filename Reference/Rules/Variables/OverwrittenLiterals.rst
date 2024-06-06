.. _variables-overwrittenliterals:

.. _overwritten-literals:

Overwritten Literals
++++++++++++++++++++

  The same variable is assigned a literal twice. It is possible that one of the assignation is too many.

This analysis doesn't take into account the distance between two assignations : it may report false positives when the variable is actually used for several purposes, and, as such, assigned twice with different values.

.. code-block:: php
   
   <?php
   
   function foo() {
       // Two assignations in a short sequence : one is too many.
       $a = 1;
       $a = 2;
       
       for($i = 0; $i < 10; $i++) {
           $a += $i;
       }
       $b = $a;
       
       // New assignation. $a is now used as an array. 
       $a = array(0);
   }
   
   ?>

Suggestions
___________

* Remove one of the assignation (the earliest)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/OverwrittenLiterals                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | literal                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


