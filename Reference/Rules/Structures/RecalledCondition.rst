.. _structures-recalledcondition:

.. _recalled-condition:

Recalled Condition
++++++++++++++++++

  A recalled condition is a check that is made twice : once in the condition, then again in the body of the structure, to collect the actual value. 

Usually, the second call may be skipped by storing the value in a local variable. à

The second call may be necessary when the call is not idempotent.

This is a speed optimisation: when the call is a simple property fetch, or include a local cache, it is a micro-optimisation. Otherwise, it has a good performance potential.

One of the option is to use an iffectation: an affectation in the condition. This serves as cache too. Otherwise, the condition may be calculated and stored before the condition.

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
* Use an iffectation in the condition, both store the result and use it in the condition.




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
| Features     | micro-optimisation, idempotent, iffectation                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


