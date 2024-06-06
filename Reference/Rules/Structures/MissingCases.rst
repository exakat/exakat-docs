.. _structures-missingcases:

.. _missing-cases-in-switch:

Missing Cases In Switch
+++++++++++++++++++++++

  It seems that some cases are missing in this switch structure.

When comparing two different `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ structures, it appears that some cases are missing in one of them. The set of cases are almost identical, but one of the values are missing. 

`Switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ structures using strings as literals are compared in this analysis. When the discrepancy between two lists is below 25%, both switches are reported.
In the example, one may argue that the 'c' case is actually handled by the 'default' case. Otherwise, business logic may request that omission.

.. code-block:: php
   
   <?php
   
   // This switch operates on a, b, c, d and default 
   switch($a) {
       case 'a': doSomethingA(); break 1;
       case 'b': doSomethingB(); break 1;
       case 'c': doSomethingC(); break 1;
       case 'd': doSomethingD(); break 1;
       default: doNothing();
   }
   
   // This switch operates on a, b, d and default 
   switch($o->p) {
       case 'a': doSomethingA(); break 1;
       case 'b': doSomethingB(); break 1;
   
       case 'd': doSomethingD(); break 1;
       default: doNothing();
   }
   
   ?>

Suggestions
___________

* Add the missing cases
* Add comments to mention that missing cases are processed in the default case




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MissingCases                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.7                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tikiwiki-structures-missingcases`                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


