.. _structures-negativepow:

.. _negative-power:

Negative Power
++++++++++++++

  The power operator `** <https://www.php.net/manual/en/language.operators.arithmetic.php>`_ has higher precedence than the sign operators + and -.

This means that -2 `** <https://www.php.net/manual/en/language.operators.arithmetic.php>`_ 2 == -4. It is in fact, -(2 `** <https://www.php.net/manual/en/language.operators.arithmetic.php>`_ 2). 

When using negative power, it is clearer to add parenthesis or to use the `pow() <https://www.php.net/pow>`_ function, which has no such ambiguity :

.. code-block:: php
   
   <?php
   
   // -2 to the power of 2 (a square)
   pow(-2, 2) == 4;
   
   // minus 2 to the power of 2 (a negative square)
   -2 ** 2 == -(2 ** 2) == 4;
   
   ?>
Connex PHP features
-------------------

  + `power <https://php-dictionary.readthedocs.io/en/latest/dictionary/power.ini.html>`_


Suggestions
___________

* Avoid negative number, as operands of **
* Use parenthesis with negative numbers and **




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NegativePow                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


