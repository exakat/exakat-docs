.. _structures-assignedinonebranch:

.. _assigned-in-one-branch:

Assigned In One Branch
++++++++++++++++++++++

  This rule reports variables that are assigned in one branch, and not in the other.

This situation means that, depending on the branch used, some variables may not always be available. Such inbalance may generate warnings. 

This rule looks at if/then structures. 


.. code-block:: php
   
   <?php
   
   if ($condition) {
       // $assigned_in_this_branch is assigned in only one of the branches
       $assigned_in_this_branch = 1;
       $also_assigned = 1;
   } else {
       // $also_assigned is assigned in the two branches
       $also_assigned = 1;
   }
   
   ?>

Suggestions
___________

* Assign in the second branch
* Assign outside the condition




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AssignedInOneBranch                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | assignation                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


