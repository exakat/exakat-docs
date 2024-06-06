.. _structures-identicalelseif:

.. _identical-elseif:

Identical Elseif
++++++++++++++++

  In a long if/elseif/then structures, identical conditions are mutually exclusive. The first one will happen, and the second will be ignored. 

This is similar to having multiple cases in the same switch or match expression.

.. code-block:: php
   
   <?php
   
   if ($a === 1) { }
   elseif ($a === 2) { }
   elseif ($a === 3) { }
   elseif ($a === 4) { }
   elseif ($a === 2) { }
   else {}
   
   ?>

Suggestions
___________

* Remove the extra elseif() clause
* Fixed the condition of the extra elseif() clause
* Use a switch() or match() expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalElseif                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | if-then                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


