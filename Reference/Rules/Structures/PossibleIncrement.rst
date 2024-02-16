.. _structures-possibleincrement:

.. _possible-increment:

Possible Increment
++++++++++++++++++

  This expression looks like a typo : a missing + would change the behavior.

The same pattern is not reported with -, as it is legit expression. + sign is usually understated, rather than explicit.


.. code-block:: php
   
   <?php
   
   // could it be a ++$b ? 
   $a = +$b;
   
   ?>

See also `Incrementing/Decrementing Operators <https://www.php.net/manual/en/language.operators.increment.php>`_ and `Arithmetic Operators <https://www.php.net/manual/en/language.operators.arithmetic.php>`_.


Suggestions
___________

* Drop the whole assignation
* Complete the addition with another value : $a = 1 + $b
* Make this a ++ operator : ++$b
* Make this a negative operator : -$b
* Make the casting explicit : (int) $b




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PossibleIncrement                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-possibleincrement`, :ref:`case-mediawiki-structures-possibleincrement`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


