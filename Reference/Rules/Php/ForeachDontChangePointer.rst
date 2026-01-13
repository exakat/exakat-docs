.. _php-foreachdontchangepointer:

.. _foreach-don't-change-pointer:

Foreach Don't Change Pointer
++++++++++++++++++++++++++++

  `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops use their own internal cursor.

A foreach loop won't change the internal pointer of the array, as it works on a copy of the source. Hence, applying array pointer's functions such as `current() <https://www.php.net/current>`_ or `next() <https://www.php.net/next>`_ to the source array won't have the same behavior in PHP 5 than PHP 7.

This only applies when a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ by reference is used.

.. code-block:: php
   
   <?php
   
   $numbers = range(1, 10);
   next($numbers);
   foreach($numbers as &$number){
       print $number;
       print current($numbers)."\n"; // Always 
   }
   
   ?>

See also `foreach no longer changes the internal array pointer <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.foreach.array-pointer>`_.

Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Do not change the pointer on the source array while in the loop




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ForeachDontChangePointer                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


