.. _php-shortternary:

.. _short-ternary:

Short Ternary
+++++++++++++

  Short ternaries are the ternary operator, where the middle operand was left out. 

Written that way, the operator checks if the first operand is empty() : in that case, the second operand is used; Otherwise, the first operand is used.  


.. code-block:: php
   
   <?php
   	// $b is now 2
   	$b = $a ?: 2;
   	// $c is now 2 also 
   	$c = $b ?: 4;
   ?>

See also `Ternary Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.ternary>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShortTernary                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`One Liners <ruleset-One-Liners>`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | short-ternary                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


