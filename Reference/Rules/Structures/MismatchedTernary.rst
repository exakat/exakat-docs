.. _structures-mismatchedternary:

.. _mismatched-ternary-alternatives:

Mismatched Ternary Alternatives
+++++++++++++++++++++++++++++++

  A ternary operator should yield the same type on both branches.

Ternary operator applies a condition, and yield two different results. Those results will then be processed by code that expects the same types. It is recommended to match the types on both branches of the ternary operator.

.. code-block:: php
   
   <?php
   
   // $object may end up in a very unstable state
   $object = ($type == 'Type') ? new $type() : null;
   
   //same result are provided by both alternative, though process is very different
   $result = ($type == 'Addition') ? $a + $b : $a * $b;
   
   //Currently, this is omitted
   $a = 1;
   $result = empty($condition) ? $a : 'default value';
   $result = empty($condition) ? $a : getDefaultValue();
   
   ?>

Suggestions
___________

* Use compatible data type in both branch of the alternative
* Turn the ternary into a if/then, with different processing




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MismatchedTernary                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Suggestions <ruleset-Suggestions>`                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.1                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpadsnew-structures-mismatchedternary`, :ref:`case-openemr-structures-mismatchedternary`                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


