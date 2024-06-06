.. _structures-noarrayunique:

.. _avoid-array\_unique():

Avoid array_unique()
++++++++++++++++++++

  The native function `array_unique() <https://www.php.net/array_unique>`_ is much slower than using other alternatives, such as `array_count_values() <https://www.php.net/array_count_values>`_, `array_flip() <https://www.php.net/array_flip>`_/`array_keys() <https://www.php.net/array_keys>`_, or even a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops.

.. code-block:: php
   
   <?php
   
   // using array_unique()
   $uniques = array_unique($someValues);
   
   // When values are strings or integers
   $uniques = array_keys(array_count_values($someValues));
   $uniques = array_flip(array_flip($someValues))
   
   //even some loops are faster.
   $uniques = [];
   foreach($someValues as $s) {
       if (!in_array($uniques, $s)) {
           $uniques[] $s;
       }
   }
   
   ?>

See also `array_unique <https://www.php.net/array_unique>`_..


Suggestions
___________

* Upgrade to PHP 7.2
* Use an alternative way to make values unique in an array, using array_count_values(), for example.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoArrayUnique                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | array                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


