.. _performances-skipemptyarray:

.. _skip-empty-array:

Skip Empty Array
++++++++++++++++

  When collecting arrays to be merged, it is faster to skip the empty arrays, rather than let `array_merge() <https://www.php.net/array_merge>`_ process them. This also works with `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_.


.. code-block:: php
   
   <?php
   
   $all = [];
   foreach($source as $array) {
   	// $array is an array in this example
   	if (empty($array)) {
   		continue;
   	}
   	
   	$all[] = $array;
   }
   
   $all = array_merge(...$all);
   
   ?>


This is a micro-optimisation. It is more efficient with larger arrays.

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SkipEmptyArray                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
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


