.. _structures-identicalconsecutive:

.. _identical-consecutive-expression:

Identical Consecutive Expression
++++++++++++++++++++++++++++++++

  Identical consecutive expressions might be double code. They are worth being checked. 

They may be a copy/paste with unmodified content. When the content has to be duplicated, it is recommended to avoid executing the expression again, and just access the cached `result <https://www.php.net/result>`_.

.. code-block:: php
   
   <?php
   
   $current  = $array[$i];
   $next     = $array[$i + 1];
   $nextnext = $array[$i + 1]; // OOps, nextnext is wrong.
   
   // Initialization
   $previous = foo($array[1]); // previous is initialized with the first value on purpose
   $next     = foo($array[1]); // the second call to foo() with the same arguments should be avoided
   // the above can be rewritten as : 
   $next     = $previous; // save the processing.
   
   for($i = 1; $i < 200; ++$i) {
       $next = doSomething();
   }
   ?>

Suggestions
___________

* Check if the expression needs to be used twice.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalConsecutive                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | expression                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


