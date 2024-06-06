.. _classes-oneobjectoperatorperline:

.. _one-object-operator-per-line:

One Object Operator Per Line
++++++++++++++++++++++++++++

  It is recommended to avoid using more than one operator -> per line, to prevent information overload.

This rule applies to chained  calls, and not on distinct expressions, that may end up on the same line. 


.. code-block:: php
   
   <?php
   
   // Spread operators on multiple lines
   $object->firstMethodCall()
          ->property
          ->secondMethodCall();
   
   // This is not readable
   $object->firstMethodCall()->property->secondMethodCall();
   
   // This is OK, as objects are different.
   $a2->b2($c2->d2, $e2->f2); 
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OneObjectOperatorPerLine                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | chain                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


