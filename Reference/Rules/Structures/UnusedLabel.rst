.. _structures-unusedlabel:

.. _unused-label:

Unused Label
++++++++++++

  Some labels have been defined in the code, but they are not used. They may be removed as they are dead code.



There is no analysis for undefined goto call, as PHP checks that goto has a destination label at compile time :

.. code-block:: php
   
   <?php
   
   $a = 0;
   A: 
   
       ++$a;
       
       // A loop. A: is used
       if ($a < 10) { goto A; }
   
   // B is never called explicitly. This is useless.
   B: 
   
   ?>

See also `Goto <https://www.php.net/manual/en/control-structures.goto.php>`_.


Suggestions
___________

* Remove the unused label
* Add a goto call to this label
* Check for spelling mistakes
* Check that it is not a coding typo, like a raw ``http://www.php.net``, left in the code (It is actually valid PHP code)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnusedLabel                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | label, goto                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


