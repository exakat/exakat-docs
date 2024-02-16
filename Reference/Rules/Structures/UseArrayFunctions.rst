.. _structures-usearrayfunctions:

.. _use-array-functions:

Use Array Functions
+++++++++++++++++++

  There are a lot of native PHP functions for arrays. It is often faster to take advantage of them than write a loop.

* `array_push() <https://www.php.net/array_push>`_ : use `array_merge() <https://www.php.net/array_merge>`_
* `array_slice() <https://www.php.net/array_slice>`_ : use `array_chunk() <https://www.php.net/array_chunk>`_
* index access : use `array_column() <https://www.php.net/array_column>`_
* append `[]`: use `array_merge() <https://www.php.net/array_merge>`_
* addition : use `array_sum() <https://www.php.net/array_sum>`_
* multiplication : use `array_product() <https://www.php.net/array_product>`_
* concatenation : use `implode() <https://www.php.net/implode>`_
* ifthen : use `array_filter() <https://www.php.net/array_filter>`_

.. code-block:: php
   
   <?php
   
   $all = implode('-', $s).'-';
   
   // same as above
   $all = '';
   foreach($array as $s) {
       $all .= $s . '-';
   }
   
   ?>

See also `Array Functions <https://www.php.net/manual/en/ref.array.php>`_ and :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`.


Suggestions
___________

* Remove the loop and use a native PHP function
* Add more expressions to the loop : batching multiple operations in one loop makes it more interesting than running separates loops.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseArrayFunctions                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


