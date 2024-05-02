.. _structures-sameconditions:

.. _same-conditions-in-condition:

Same Conditions In Condition
++++++++++++++++++++++++++++

  At least two consecutive if/then structures use identical conditions. The latter will probably be ignored.

This analysis returns false positive when there are attempt to fix a situation, or to call an alternative solution. 

Conditions that are shared between if structures, but inside a logical OR expression are also detected.

.. code-block:: php
   
   <?php
   
   if ($a == 1) { doSomething(); }
   elseif ($b == 1) { doSomething(); }
   elseif ($c == 1) { doSomething(); }
   elseif ($a == 1) { doSomething(); }
   else {}
   
   // Also works on if then else if chains
   if ($a == 1) { doSomething(); }
   else if ($b == 1) { doSomething(); }
   else if ($c == 1) { doSomething(); }
   else if ($a == 1) { doSomething(); }
   else {}
   
   // Also works on if then else if chains
   // Here, $a is common and sufficient in both conditions
   if ($a || $b) { doSomething(); } 
   elseif ($a || $c) { doSomethingElse(); } 
   
   // This sort of situation generate false postive. 
   $config = load_config_from_commandline();
   if (empty($config)) {
       $config = load_config_from_file();
       if (empty($config)) {
           $config = load_default_config();
       }
   }
   
   ?>

Suggestions
___________

* Merge the two conditions into one
* Make the two conditions different




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SameConditions                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-structures-sameconditions`, :ref:`case-typo3-structures-sameconditions`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


