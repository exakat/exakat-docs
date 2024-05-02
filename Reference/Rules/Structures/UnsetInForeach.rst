.. _structures-unsetinforeach:

.. _unset-in-foreach:

Unset In Foreach
++++++++++++++++

  Unset applied to the variables of a ``foreach`` loop are useless. Those variables are copies and not the actual value. Even if the value is a reference, unsetting it has no effect on the original array : the only effect may be indirect, on elements inside an array, or on properties inside an object.

.. code-block:: php
   
   <?php
   
   // When unset is useless
   $array = [1, 2, 3];
   foreach($array as $a) {
       unset($a);
   }
   
   print_r($array); // still [1, 2, 3]
   
   foreach($array as $b => &$a) {
       unset($a);
   }
   
   print_r($array); // still [1, 2, 3]
   
   // When unset is useful
   $array = [ [ 'c' => 1] ]; // Array in array
   foreach($array as &$a) {
       unset(&$a['c']);
   }
   
   print_r($array); // now [ ['c' => null] ]
   
   ?>

Suggestions
___________

* Drop the unset




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnsetInForeach                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Dead code <ruleset-Dead-code>`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | foreach                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


