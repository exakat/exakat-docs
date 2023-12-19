.. _structures-arraymergearrayarray:

.. _array\_merge-needs-array-of-arrays:

Array_merge Needs Array Of Arrays
+++++++++++++++++++++++++++++++++

  When collecting data to feed `array_merge() <https://www.php.net/array_merge>`_, use an array of array as default value. ```array(`array()) <https://www.php.net/array>`_``` is the neutral value for `array_merge() <https://www.php.net/array_merge>`_;

This analysis also reports when the used types are not an array : `array_merge() <https://www.php.net/array_merge>`_ does not accept scalar values, but only arrays.


.. code-block:: php
   
   <?php
   
   // safe default value
   $a = array(array());
   
   // when $list is empty, it is 
   foreach($list as $l) {
       $a[] = $l;
   }
   $b = array_merge($a);
   
   ?>


Since PHP 7.4, it is possible to call `array_merge() <https://www.php.net/array_merge>`_ without an argument : this means the default value may an empty array. This array shall not contain scalar values.

See also `array_merge <https://www.php.net/array_merge>`_.


Suggestions
___________

* Use ```array(array())``` or ```[[]]``` as default value for array_merge()
* Remove any non-array value from the values in the default array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeArrayArray                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | array                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


