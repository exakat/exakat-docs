.. _structures-uselesscoalesce:

.. _useless-coalesce:

Useless Coalesce
++++++++++++++++

  The ?: operator needs the condition to be potentially empty. This means that the type should have the possibility to be null, false, 0, or any of the empty values.

.. code-block:: php
   
   <?php
   
   function foo(A $a, bool $b) {
   	$a ?: 'a';
   	$b ?: 'a';
   }
   
   ?>

Suggestions
___________

* Remove the operator.
* Extend the type to include values that may be empty.




Specs
_____

+--------------+------------------------------------------------------------+
| Short name   | Structures/UselessCoalesce                                 |
+--------------+------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>` |
+--------------+------------------------------------------------------------+
| Exakat since | 2.6.6                                                      |
+--------------+------------------------------------------------------------+
| Severity     | Minor                                                      |
+--------------+------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                            |
+--------------+------------------------------------------------------------+
| Precision    | High                                                       |
+--------------+------------------------------------------------------------+
| Available in |                                                            |
+--------------+------------------------------------------------------------+


