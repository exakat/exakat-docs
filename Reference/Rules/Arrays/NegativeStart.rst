.. _arrays-negativestart:

.. _negative-start-index-in-array:

Negative Start Index In Array
+++++++++++++++++++++++++++++

  Negative starting index in arrays changed in PHP 8.0. Until then, they were ignored, and automatic index started always at 0. Since PHP 8.0, the next index is calculated.

The behavior will `break <https://www.php.net/manual/en/control-structures.break.php>`_ code that relies on automatic index in arrays, when a negative index is used for a starter.

.. code-block:: php
   
   <?php
   
   $x = [-5 => 2];
   $x[] = 3;
   
   print_r($x);
   
   /*
   PHP 7.4 and older 
   Array
   (
       [-5] => 2
       [0] => 3
   )
   */
   
   /*
   PHP 8.0 and more recent
   Array
   (
       [-5] => 2
       [-4] => 3
   )
   */
   
   ?>

See also `PHP RFC: Arrays starting with a negative index <https://wiki.php.net/rfc/negative_array_index>`_.


Suggestions
___________

* Explicitly create the index, instead of using the automatic indexing
* Add an explicit index of 0 in the initial array, to set the automatic process in the right track
* Avoid using specified index in array, conjointly with automatic indexing.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Arrays/NegativeStart                                                                                                                                                                    |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.1.9                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                              |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features         | index                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


