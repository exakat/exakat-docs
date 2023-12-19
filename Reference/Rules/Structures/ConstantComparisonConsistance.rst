.. _structures-constantcomparisonconsistance:

.. _constant-comparison:

Constant Comparison
+++++++++++++++++++

  Constant to the left or right is a favorite. 

Comparisons are commutative : they may be $a == B or B == $a. The analyzed code show less than 10% of one of the two : for consistency reasons, it is recommended to make them all the same. 

Putting the constant on the left is also called 'Yoda Comparison', as it mimics the famous characters style of speech. It prevents errors like 'B = $a' where the comparison is turned into an assignation. 

The natural way is to put the constant on the right. It is often less surprising. 

Every comparison operator is used when finding the favorite.

.. code-block:: php
   
   <?php
   
   // 
   if ($a === B) { doSomething(); }
   if ($c > D) { doSomething(); }
   if ($e !== G) { doSomething(); }
   do { doSomething(); } while ($f === B);
   while ($a === B) { doSomething(); }
   
   // be consistent
   if (B === $a) {}
   
   // Compari
   if (B <= $a) {}
   
   ?>

Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConstantComparisonConsistance                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Preferences <ruleset-Preferences>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Features     | comparison                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_    |
+--------------+----------------------------------------------------------------------------------------------------------------------------+


