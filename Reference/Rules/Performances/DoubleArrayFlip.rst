.. _performances-doublearrayflip:

.. _double-array\_flip():

Double array_flip()
+++++++++++++++++++

  Avoid double `array_flip() <https://www.php.net/array_flip>`_ to gain speed. While `array_flip() <https://www.php.net/array_flip>`_ alone is usually useful, a double call to `array_flip() <https://www.php.net/array_flip>`_ is made to make values and keys unique. 


.. code-block:: php
   
   <?php
   
   // without array_flip
   function foo($array, $value) {
       $key = array_search($array, $value);
       
       if ($key !== false) {
           unset($array[$key]);
       }
       
       return $array;
   }
   
   // double array_flip
   // array_flip() usage means that $array's values are all unique
   function foo($array, $value) {
       $flipped = array_flip($value);
       unset($flipped[$value]);
       return array_flip($flipped);
   }
   
   ?>

Suggestions
___________

* Use array_unique() or array_count_values().
* Use array_flip() once, and let PHP garbage collect it later.
* Keep the original values in a separate variable.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/DoubleArrayFlip                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-performances-doublearrayflip`                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


