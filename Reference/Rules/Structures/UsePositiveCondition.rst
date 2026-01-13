.. _structures-usepositivecondition:

.. _use-positive-condition:

Use Positive Condition
++++++++++++++++++++++

  Whenever possible, use a positive condition. 

Positive conditions are easier to understand, and lead to less understanding problems.
Negative conditions are not reported when else is not present.

.. code-block:: php
   
   <?php
   
   // This is a positive condition
   if ($a == 'b') {
       doSomething();
   } else {
       doSomethingElse();
   }
   
   if (!empty($a)) {
       doSomething();
   } else {
       doSomethingElse();
   }
   
   // This is a negative condition
   if ($a == 'b') {
       doSomethingElse();
   } else {
       doSomething();
   }
   
   // No need to force $a == 'b' with empty else
   if ($a != 'b') {
       doSomethingElse();
   } 
   
   ?>

See also `Double negatives should not not be avoided <https://cleankotlin.nl/blog/double-negations>`_ and `How To Write Conditional Statements in PHP <https://www.digitalocean.com/community/tutorials/how-to-write-conditional-statements-in-php>`_.


Suggestions
___________

* Invert the code in the if branches, and the condition




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UsePositiveCondition                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-structures-usepositivecondition`, :ref:`case-expressionengine-structures-usepositivecondition`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


