.. _structures-oneexpressionbracketsconsistency:

.. _one-expression-brackets-consistency:

One Expression Brackets Consistency
+++++++++++++++++++++++++++++++++++

  Brackets around one-line expressions are not consistent. 

PHP makes bracket optional when a control structure pilot only one expression. Both are semantically identical.

This analysis reports code that uses brackets while the vast majority of other expressions uses none. Or the contrary. 


.. code-block:: php
   
   <?php
   
   // One expression with brackets
   for($i = 0; $i < 10; $i++) { $c++; }
   
   // One expression without bracket
   for($i2 = 0; $i2 < 10; $i2++)  $c++; 
   
   ?>


Another analysis, [Structures/Bracketless], reports the absence of brackets as an `error <https://www.php.net/error>`_.

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneExpressionBracketsConsistency                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


