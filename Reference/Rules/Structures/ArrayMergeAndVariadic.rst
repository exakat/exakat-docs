.. _structures-arraymergeandvariadic:

.. _array\_merge()-and-variadic:

array_merge() And Variadic
++++++++++++++++++++++++++

  Always check value in variadic before using it with `array_merge() <https://www.php.net/array_merge>`_ and `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_.

Before PHP 7.4, `array_merge() <https://www.php.net/array_merge>`_ and `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_ would complain when no argument was provided. As such, using the spread operator `...` on an empty `array() <https://www.php.net/array>`_ would yield no argument, and an `error <https://www.php.net/error>`_.


.. code-block:: php
   
   <?php
   
   $b = array_merge(...$x);
   
   ?>

Suggestions
___________

* Add a check to the spread variable to ensure it is not empty
* Append an empty array to to the spread variable to ensure it is not empty




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeAndVariadic                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | variadic                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


