.. _structures-suspiciouscomparison:

.. _suspicious-comparison:

Suspicious Comparison
+++++++++++++++++++++

  The comparison seems to be misplaced.

A comparison happens in the last argument, while the actual function expect another type : this may be the case of a badly placed parenthesis.
Original idea by `Vladimir Reznichenko <https://twitter.com/kalessil>`_.

.. code-block:: php
   
   <?php
   
   // trim expect a string, a boolean is given.
   if (trim($str === '')){
   
   }
   
   // Just move the first closing parenthesis to give back its actual meaning
   if (trim($str) === ''){
   
   }
   
   ?>

Suggestions
___________

* Remove the comparison altogether
* Move the comparison to its right place : that, or more the parenthesis.
* This may be what is intended : just leave it.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SuspiciousComparison                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | comparison                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpipam-structures-suspiciouscomparison`, :ref:`case-expressionengine-structures-suspiciouscomparison`       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


