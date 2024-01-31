.. _structures-iszero:

.. _is-actually-zero:

Is Actually Zero
++++++++++++++++

  This addition actually may be simplified because one term is actually negated by another. 

This kind of `error <https://www.php.net/error>`_ happens when the expression is very large : the more terms are included, the more chances are that some auto-annihilation happens. 

This `error <https://www.php.net/error>`_ may also be a simple typo : for example, calculating the difference between two consecutive terms.

.. code-block:: php
   
   <?php
   
   // This is quite obvious
   $a = 2 - 2;
   
   // This is obvious too. This may be a typo-ed difference between two consecutive terms. 
   // Could have been $c = $fx[3][4] - $fx[3][3] or $c = $fx[3][5] - $fx[3][4];
   $c = $fx[3][4] - $fx[3][4];
   
   // This is less obvious
   $a = $b[3] - $c + $d->foo(1,2,3) + $c + $b[3];
   
   ?>

Suggestions
___________

* Clean the code and remove the null sum
* Fix one of the variable : this expression needs another variable here
* When adding differences, calculate the difference in a temporary variable first.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IsZero                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.15                                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-iszero`, :ref:`case-suitecrm-structures-iszero`                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


