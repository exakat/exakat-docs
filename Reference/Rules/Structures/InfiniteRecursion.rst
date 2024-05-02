.. _structures-infiniterecursion:

.. _infinite-recursion:

Infinite Recursion
++++++++++++++++++

  A method is calling itself, with unchanged arguments. This might repeat indefinitely.

This rules applies to recursive functions without any condition. This also applies to function which inject the incoming arguments, without modifications.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       if ($a > 10) {
           return;
       }
       foo($a, $b);
   }
   
   function foo2($a, $b) {
       ++$a;   // $a is modified
       if ($a > 10) {
           return;
       }
       foo2($a, $b);
   }
   
   ?>

Suggestions
___________

* Modify arguments before injecting them again in the same method
* Use different values when calling the same method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InfiniteRecursion                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | loop, recursion, infinite                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


