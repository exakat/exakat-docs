.. _structures-arraymergewithellipsis:

.. _array\_merge-with-ellipsis:

array_merge With Ellipsis
+++++++++++++++++++++++++

  Ellipsis, or `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_, returns a null when the operand array is empty. This doesn't suit `array_merge() <https://www.php.net/array_merge>`_. 

It is recommended to use a coalesce operator, to handle graciously an empty array : use an empty array as default value.

This applies to the following PHP functions : 

* `array_merge() <https://www.php.net/array_merge>`_
* `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_
* `array_diff() <https://www.php.net/array_diff>`_
* `array_diff_assoc() <https://www.php.net/array_diff_assoc>`_
* `array_diff_key() <https://www.php.net/array_diff_key>`_
* `array_diff_uassoc() <https://www.php.net/array_diff_uassoc>`_


.. code-block:: php
   
   <?php
   
   // Correct usage of array_merge and ellipsis
   $a = [ [1,2], [3,4]];
   $b = array_merge(...$a);
   
   // Notee the nested array
   $a = [ ];
   $b = array_merge(...$a ?: [[]] );
   
   // Yield an error because $a is empty
   $a = [ ];
   $b = array_merge(...$a);
   
   ?>

Suggestions
___________

* Use one of the coalesce operator to default to an empty array, avoiding a runtime warning.
* Check the content of the expanded array before using it




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeWithEllipsis                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.6                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


