.. _dump-dumpcomparedliterals:

.. _collect-compared-literals:

Collect Compared Literals
+++++++++++++++++++++++++

  This collects the different literals (null, integers, floats, strings) that are used in comparisons. 

Comparisons include all the comparison operators : <, >, <=, >=, !=, <>, ==.

This analysis also covers `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_, `array_keys() <https://www.php.net/array_keys>`_ and `in_array() <https://www.php.net/in_array>`_. 

Strict searches are omitted. So, ===, !==, `match() <https://www.php.net/manual/en/control-structures.match.php>`_, `in_array() <https://www.php.net/in_array>`_ and `array_keys() <https://www.php.net/array_keys>`_ with 3rd parameter are omitted.

Some comparisons are not covered yet : `sort() <https://www.php.net/sort>`_.


.. code-block:: php
   
   <?php
   
   // Collects '>' and 3
   if ($x > 3) {
   	// doSomething()
   }
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/DumpComparedLiterals                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dump <ruleset-Dump>`                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


