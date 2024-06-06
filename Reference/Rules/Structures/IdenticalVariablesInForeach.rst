.. _structures-identicalvariablesinforeach:

.. _identical-variables-in-foreach:

Identical Variables In Foreach
++++++++++++++++++++++++++++++

  Do not use the same variable names as a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ source and one of its blind variables. 

`Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ makes a copy of the original data while working on it : this prevents any interference. Yet, when the source and the blind variable is the same, the source will have changed after the loop.

.. code-block:: php
   
   <?php
   
   // classic way to use a foreach loop
   foreach($array as $key => $value) {
       // doSomething with $key and $value
   }
   
   // unusual way to end up with a name conflict
   foreach($a as $a => [$b, $c, $a]) {
       // doSomething with $a and $a, $b, $c
   }
   
   
   // classic way to use a foreach loop
   foreach($a as $a => $b) {
       // doSomething with $a and $a
   }
   // Now, after the loop, $a is an integer or a string!
   
   ?>

Suggestions
___________

* Use a different name for the source of the array and the blind values




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalVariablesInForeach                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | foreach                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


