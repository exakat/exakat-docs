.. _performances-optimizeexplode:

.. _optimize-explode():

Optimize Explode()
++++++++++++++++++

  Limit `explode() <https://www.php.net/explode>`_ results at call time. `explode() <https://www.php.net/explode>`_ returns an array, after breaking the argument into smaller strings, with a delimiter. 

By default, `explode() <https://www.php.net/explode>`_ breaks the whole string into smaller strings, and returns the array. When not all the elements of the returned array are necessary, using the third argument of `explode() <https://www.php.net/explode>`_ speeds up the process, by removing unnecessary work.


.. code-block:: php
   
   <?php
   
   $string = '1,2,3,4,5,';
   
   // explode() returns 2 elements, which are then assigned to the list() call.
   list($a, $b) = explode(',', $string, 2);
   
   // explode() returns 6 elements, only two of which are then assigned to the list() call. The rest are discarded.
   list($a, $b) = explode(',', $string, 2);
   
   // it is not possible to skip the first elements, but it is possible to skip the last ones. 
   echo explode(',', $string, 2)[1];
   
   // This protects PHP, in case $string ends up with a lot of commas
   $string = foo(); // usually '1,2' but not known
   list($a, $b) = explode(',', $string, 2);
   ?>


Limiting `explode() <https://www.php.net/explode>`_ has no effect when the operation is already exact : it simply prevents `explode() <https://www.php.net/explode>`_ to cut more than needed if the argument is unexpectedly large. 

This optimisation applies to split(), `preg_split() <https://www.php.net/preg_split>`_ and `mb_split() <https://www.php.net/mb_split>`_, too.

This is a micro optimisation, unless the exploded string is large.

See also `Cryptography Extensions <https://www.php.net/manual/en/refs.crypto.php>`_.


Suggestions
___________

* Add a limit to explode() call




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/OptimizeExplode                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | crypto                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


