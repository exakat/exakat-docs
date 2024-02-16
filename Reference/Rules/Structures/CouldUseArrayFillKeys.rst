.. _structures-couldusearrayfillkeys:

.. _could-use-array\_fill\_keys:

Could Use array_fill_keys
+++++++++++++++++++++++++

  `array_fill_keys() <https://www.php.net/array_fill_keys>`_ is a native PHP function that creates an array from keys. It gets the list of keys, and a constant value to assign to each keys.

This is twice faster than doing the same with a loop.

Note that is possible to use an object as initializing value : every element of the final array will be pointing to the same value. And, also, using an object as initializing value means that the same object will be used for each key : the object will not be cloned for each value.

.. code-block:: php
   
   <?php
   
   $array = range('a', 'z');
   
   // Fast way to build the array
   $b = array_fill_keys($a, 0);
   
   // Fast way to build the array, but every element will be the same object
   $b = array_fill_keys($a, new Stdclass());
   
   // Slow way to build the array
   foreach($array as $a) {
       $b[$a] = 0;
   }
   
   // Setting everything to null, slowly
   $array = array_map(function() {}, $array);
   
   ?>

See also `array_fill_keys <https://www.php.net/array_fill_keys>`_.


Suggestions
___________

* Use array_fill_keys()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseArrayFillKeys                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-structures-couldusearrayfillkeys`, :ref:`case-phpipam-structures-couldusearrayfillkeys`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


