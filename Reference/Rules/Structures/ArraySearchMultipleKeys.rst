.. _structures-arraysearchmultiplekeys:

.. _searching-for-multiple-keys:

Searching For Multiple Keys
+++++++++++++++++++++++++++

  `array_search() <https://www.php.net/array_search>`_ and `array_keys() <https://www.php.net/array_keys>`_ find keys in an array. `array_search() <https://www.php.net/array_search>`_ returns the first key that match a value, while `array_keys() <https://www.php.net/array_keys>`_ returns all the keys that match a value.

`array_search() <https://www.php.net/array_search>`_ and `array_keys() <https://www.php.net/array_keys>`_ both accepts a final parameter to set a strict search or not.

.. code-block:: php
   
   <?php
   
   $array = array(0,1,2,3,4,3);
   
   // $id = 3
   $id = array_search($array, 3);
   
   // $ids = [3, 5];
   $ids = array_keys($array, 3);
   
   ?>

Suggestions
___________

* Use array_keys() to find multiple keys in an array
* Use array_keys() to find a unique key in an array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArraySearchMultipleKeys                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


