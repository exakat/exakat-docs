.. _structures-usecountrecursive:

.. _use-count-recursive:

Use Count Recursive
+++++++++++++++++++

  The code could use the recursive version of count.

The second argument of count, when set to ``COUNT_RECURSIVE``, count recursively the elements. It also counts the elements themselves.

.. code-block:: php
   
   <?php
   
   $array = array( array(1,2,3), array(4,5,6));
   
   print (count($array, COUNT_RECURSIVE) - count($array, COUNT_NORMAL));
   
   $count = 0;
   foreach($array as $a) {
       $count += count($a);
   }
   print $count;
   
   ?>

See also `count <https://www.php.net/count>`_.


Suggestions
___________

* Drop the loop and use the 2nd argument of count()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseCountRecursive                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-structures-usecountrecursive`, :ref:`case-prestashop-structures-usecountrecursive`                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


