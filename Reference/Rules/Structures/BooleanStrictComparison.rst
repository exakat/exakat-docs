.. _structures-booleanstrictcomparison:

.. _strict-comparison-with-booleans:

Strict Comparison With Booleans
+++++++++++++++++++++++++++++++

  Strict comparisons prevent mistaking an `error <https://www.php.net/error>`_ with a false. 

Boolean values may be easily mistaken with other values, especially when the function may return integer or boolean as a normal course of action. 

It is encouraged to use strict comparison === or !== when booleans are involved in a comparison.
`switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ structures always uses `==` comparisons. Since PHP 8.0, it is possible to use `match() <https://www.php.net/manual/en/control-structures.match.php>`_ to have strict comparisons. This is not reported by this analysis, as every switch should be refactored. 

Native functions `in_array() <https://www.php.net/in_array>`_, `array_keys() <https://www.php.net/array_keys>`_ and `array_search() <https://www.php.net/array_search>`_ have a third parameter to make it use strict comparisons.

.. code-block:: php
   
   <?php
   
   // distinguish between : $b isn't in $a, and, $b is at the beginning of $a 
   if (strpos($a, $b) === 0) {
       doSomething();
   }
   
   // DOES NOT distinguish between : $b isn't in $a, and, $b is at the beginning of $a 
   if (strpos($a, $b)) {
       doSomething();
   }
   
   // will NOT mistake 1 and true
   $a = array(0, 1, 2, true);
   if (in_array($a, true, true)) {
       doSomething();
   }
   
   // will mistake 1 and true
   $a = array(0, 1, 2, true);
   if (in_array($a, true)) {
       doSomething();
   }
   
   ?>

Suggestions
___________

* Use strict comparison whenever possible




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BooleanStrictComparison                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | strict-comparison, switch, match                                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-structures-booleanstrictcomparison`, :ref:`case-typo3-structures-booleanstrictcomparison`                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


