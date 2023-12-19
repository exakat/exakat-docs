.. _performances-ellipsismerge:

.. _ellipsis-merge:

Ellipsis Merge
++++++++++++++

  Ellipsis are slower than `array_merge() <https://www.php.net/array_merge>`_. 


.. code-block:: php
   
   <?php
   
   // slow
   $all = array_merge($array1, $array2);
   
   // very slow
   $all = array(...$array1, ...$array2);
   
   ?>


This is a micro optimisation. The larger and numerous the arrays, the better the speed gain. 

The speed up is significative when the merge happen inside a loop. There, `array_merge() <https://www.php.net/array_merge>`_ is an order of magnitude faster.

Suggestions
___________

* Use array_merge()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/EllipsisMerge                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | merge, ellipsis, micro-optimisation                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


