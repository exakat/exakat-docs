.. _structures-dontchangeblindkey:

.. _don't-change-the-blind-var:

Don't Change The Blind Var
++++++++++++++++++++++++++

  When using a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_, the blind variables hold a copy of the original value. It is confusing to modify them, as it seems that the original value may be changed.

When actually changing the original value, use the reference in the foreach definition to make it obvious, and save the final reassignation.

When the value has to be prepared before usage, then save the filtered value in a separate variable. This makes the clean value obvious, and preserve the original value for a future usage.


.. code-block:: php
   
   <?php
   
   // $bar is duplicated and kept 
   $foo = [1, 2, 3];
   foreach($foo as $bar) {
       // $bar is updated but its original value is kept
       $nextBar = $bar + 1;
       print $bar . ' => ' . ($nextBar) . PHP_EOL;
       foobar($nextBar);
   }
   
   // $bar is updated and lost
   $foo = [1, 2, 3];
   foreach($foo as $bar) {
       // $bar is updated but its final value is lost
       print $bar . ' => ' . (++$bar) . PHP_EOL;
       // Now that $bar is reused, it is easy to confuse its value
       foobar($bar);
   }
   
   // $bar is updated and kept
   $foo = [1, 2, 3];
   foreach($foo as &$bar) {
       // $bar is updated and keept
       print $bar . ' => ' . (++$bar) . PHP_EOL;
       foobar($bar);
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontChangeBlindKey                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | loop, blind-key                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


