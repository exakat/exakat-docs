.. _structures-nomaxonemptyarray:

.. _no-max-on-empty-array:

No Max On Empty Array
+++++++++++++++++++++

  Using `max() <https://www.php.net/max>`_ or `min() <https://www.php.net/min>`_ on an empty array leads to a ``valueError`` `exception <https://www.php.net/exception>`_.

Until PHP 8, `max() <https://www.php.net/max>`_ and `min() <https://www.php.net/min>`_ would return null in case of empty array. This might be confusing with actual values, as an array can contain ``null``. ``null`` has a specific behavior when comparing with other values, and should be avoided with `max() <https://www.php.net/max>`_ and sorts. 


.. code-block:: php
   
   <?php
   
   // Throws a value error
   $a = max([]);
   
   $array = [];
   if (empty($array)) {
   	$a = null;
   } else {
   	$a = max($array);
   }
   
   
   var_dump(min([-1,  null])); // NULL
   var_dump(max([-1,  null])); // -1
   var_dump(max([1,  null]));  // 1
   
   ?>


Until PHP 8.0, a call on an empty array would return null, and a warning.

Suggestions
___________

* Check the content of the array before giving it to max() or min()




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/NoMaxOnEmptyArray                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.5.2                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


