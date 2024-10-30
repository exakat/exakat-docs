.. _structures-inconsistentelseif:

.. _inconsistent-elseif:

Inconsistent Elseif
+++++++++++++++++++

  Chaining if/elseif requires a consistent string of conditions. The conditions are executed one after the other, and the conditions shouldn't overlap.

This analysis reports chains of elseif that don't share a common variable (or array, or property, etc.. ). As such, testing different conditions are consistent.

.. code-block:: php
   
   <?php
   
   // $a is always common, so situations are mutually exclusive
   if ($a === 1) {
       doSomething();
   } else if ($a > 1) {
       doSomethingElse();
   } else {
       doSomethingDefault();
   }
   
   // $a is always common, so situations are mutually exclusive
   // although, it may be worth checking the consistency here
   if ($a->b === 1) {
       doSomething();
   } else if ($a->c > 1) {
       doSomethingElse();
   } else {
       doSomethingDefault();
   }
   
   // if $a === 1, then $c doesn't matter? 
   // This happens, but then logic doesn't appear in the code.
   if ($a === 1) {
       doSomething();
   } else if ($c > 1) {
       doSomethingElse();
   } else {
       doSomethingDefault();
   }
   
   ?>
Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InconsistentElseif                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


