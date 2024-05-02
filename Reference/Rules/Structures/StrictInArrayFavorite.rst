.. _structures-strictinarrayfavorite:

.. _strict-in\_array()-preference:

Strict In_Array() Preference
++++++++++++++++++++++++++++

  It is possible to set `in_array() <https://www.php.net/in_array>`_ to strict search mode, by using the third argument.

The analyzed code has less than 10% of one of the two sets : for consistency reasons, it is recommended to make them all the same. 

Warning : the two sets of operators have different precedence levels. Using and or && is not exactly the same, especially and not only, when assigning the results to a variable. 
In doubt, it is recommended to use the strict mode.

.. code-block:: php
   
   <?php 
   
   // relax mode : value may use typejuggling with the array values
   in_array($value, $array );
   
   // strict mode : value is compared to array's value with both data and type
   in_array($value, $array, true);
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StrictInArrayFavorite                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | strict-comparison                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


