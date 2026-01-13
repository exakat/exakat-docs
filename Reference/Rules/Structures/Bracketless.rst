.. _structures-bracketless:

.. _bracketless-blocks:

Bracketless Blocks
++++++++++++++++++

  PHP allows one liners as `for() <https://www.php.net/manual/en/control-structures.for.php>`_, `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_, `while() <https://www.php.net/manual/en/control-structures.while.php>`_, do/`while() <https://www.php.net/manual/en/control-structures.while.php>`_ loops, or as then/else expressions. 

It is generally considered a bad practice, as readability is lower and there are non-negligible risk of excluding from the loop the next instruction.
`switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ and `match() <https://www.php.net/manual/en/control-structures.match.php>`_ cannot be without bracket.

.. code-block:: php
   
   <?php
   
   // Legit one liner
   foreach(range('a', 'z') as $letter) ++$letterCount;
   
   // More readable version, even for a one liner.
   foreach(range('a', 'z') as $letter) {
       ++$letterCount;
   }
   
   ?>

Suggestions
___________

* Assign in the second branch
* Assign outside the condition




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Bracketless                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


