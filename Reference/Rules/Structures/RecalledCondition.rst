.. _structures-recalledcondition:

.. _recalled-condition:

Recalled Condition
++++++++++++++++++

  A recalled condition is a check that is made twice : once in the condition, once in the body of the structure. 

Usually, the second call may be skipped by storing the value in a local variable. 
The second call may be necessary when the call is not idempotent.

.. code-block:: php
   
   <?php
   
   if (get('a')) {
   	$a = get('a');
   	echo "Here is a : $a\n";
   }
   
   ?>

Suggestions
___________

* Put the result of the call in a variable to cache it.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RecalledCondition                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | micro-optimisation, idempotent                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


