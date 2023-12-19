.. _structures-staticloop:

.. _static-loop:

Static Loop
+++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ loop may be preprocessed.

It looks like the following loops are `static <https://www.php.net/manual/en/language.oop5.static.php>`_ : the same code is executed each time, without taking into account loop variables.


.. code-block:: php
   
   <?php
   
   // Static loop
   $total = 0;
   for($i = 0; $i < 10; $i++) {
       $total += $i;
   }
   
   // The above loop may be replaced by (with some math help)
   $total = 10 * (10  + 1) / 2;
   
   // Non-Static loop (the loop depends on the size of the array)
   $n = count($array);
   for($i = 0; $i < $n; $i++) {
       $total += $i;
   }
   
   ?>


It is possible to create loops that don't use any blind variables, though this is fairly rare. In particular, calling a method may update an internal pointer, like `next() <https://www.php.net/next>`_ or ``SimpleXMLIterator\:\:`next() <https://www.php.net/next>`_``. 

It is recommended to turn a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ loop into an expression that avoid the loop. For example, replacing the sum of all integers by the ``function $n * ($n + 1) / 2``, or using `array_sum() <https://www.php.net/array_sum>`_.

This analysis doesn't detect usage of variables with ``compact``.

Suggestions
___________

* Precalculate the result of that loop and removes it altogether
* Check that the loop is not missing a blind variable usage
* Replace the usage of a loop with a native PHP call : for example, with str_repeat(). Although the loop is still here, it usually reflects better the intend.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StaticLoop                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | loop                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


