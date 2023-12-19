.. _performances-noconcatinloop:

.. _avoid-concat-in-loop:

Avoid Concat In Loop
++++++++++++++++++++

  Concatenations inside a loop generate a lot of temporary variables. They are accumulated and tend to raise the memory usage, leading to slower performances.

It is recommended to store the values in an array, and then use `implode() <https://www.php.net/implode>`_ on that array to make the concatenation at once. The effect is positive when the source array has at least 50 elements. 


.. code-block:: php
   
   <?php
   
   // Concatenation in one operation
   $tmp = array();
   foreach(data_source() as $data) {
       $tmp[] = $data;
   }
   $final = implode('', $tmp);
   
   // Concatenation in many operations
   foreach(data_source() as $data) {
       $final .= $data;
   }
   
   ?>


The same doesn't apply to addition and multiplication, with `array_sum() <https://www.php.net/array_sum>`_ and array_multiply(), as those operations work on the current memory allocation, and don't need to allocate new memory at each step.

See also `PHP 7 performance improvements (3/5): Encapsed strings optimization <https://blog.blackfire.io/php-7-performance-improvements-encapsed-strings-optimization.html>`_.


Suggestions
___________

* Collect all pieces in an array, then implode() the array in one call.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/NoConcatInLoop                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`, :ref:`Top10 <ruleset-Top10>`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | loop                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-performances-noconcatinloop`, :ref:`case-thinkphp-performances-noconcatinloop`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


