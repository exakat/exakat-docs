.. _structures-wrongprecedenceinexpression:

.. _wrong-precedence-in-expression:

Wrong Precedence In Expression
++++++++++++++++++++++++++++++

  These operators are not executed in the expected order. Coalesce and ternary operator have lesser precedence compared to comparisons or spaceship operators. 

Thus, the comparison is executed first, and the other operator later. 

It is recomended to use parenthesis in these cases.

Note that this may behave as expected, with a bit of clever placing boolean: see last example.

.. code-block:: php
   
   <?php
   
   // This 
   if ($a ?? 1 == 2) {} 
   
   // is equivalent to 
   if ($a ?? (1 == 2)) {} 
   
   // It is different from
   if (($a ?? 1) == 2) {} 
   
   // This one is also wrong, but falls back on correct values
   if ($a ?? false === true) {} 
   
   ?>

Suggestions
___________

* Add parenthesis around the coalesce operator




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/WrongPrecedenceInExpression                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Available in |                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------+


