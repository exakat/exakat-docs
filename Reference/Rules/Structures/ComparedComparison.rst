.. _structures-comparedcomparison:

.. _compared-comparison:

Compared Comparison
+++++++++++++++++++

  Usually, comparison are sufficient, and it is rare to have to compare the `result <https://www.php.net/result>`_ of comparison. Check if this two-stage comparison is really needed.

.. code-block:: php
   
   <?php
   
   if ($a === strpos($string, $needle) > 2) {}
   
   // the expression above apply precedence : 
   // it is equivalent to : 
   if (($a === strpos($string, $needle)) > 2) {}
   
   ?>

See also `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ComparedComparison                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | comparison                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


