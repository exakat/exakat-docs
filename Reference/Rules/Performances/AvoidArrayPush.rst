.. _performances-avoidarraypush:

.. _avoid-array\_push():

Avoid array_push()
++++++++++++++++++

  `array_push() <https://www.php.net/array_push>`_ is slower than the append ``[]`` operator.

This is also true when the append operator is called several times, while `array_push() <https://www.php.net/array_push>`_ is be called only once, with an arbitrary number of argument. 

Using count after the push is also faster than collecting `array_push() <https://www.php.net/array_push>`_ return value. 


.. code-block:: php
   
   <?php
   
   $a = [1,2,3];
   // Fast version
   $a[] = 4;
   
   $a[] = 5;
   $a[] = 6;
   $a[] = 7;
   $count = count($a);
   
   // Slow version
   array_push($a, 4);
   $count = array_push($a, 5,6,7);
   
   // Multiple version : 
   $a[] = 1;
   $a[] = 2;
   $a[] = 3;
   array_push($a, 1, 2, 3);
   
   ?>


It is a micro-optimisation.

Suggestions
___________

* Use the [] operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/AvoidArrayPush                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


