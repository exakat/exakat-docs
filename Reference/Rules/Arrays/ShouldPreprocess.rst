.. _arrays-shouldpreprocess:

.. _preprocess-arrays:

Preprocess Arrays
+++++++++++++++++

  Using long list of assignations for initializing arrays is significantly slower than the declaring them as an array. 

If the array has to be completed rather than created, it is also faster to use += when there are more than ten elements to add.

.. code-block:: php
   
   <?php
   
   // Slow way
   $a = []; // also with $a = array();
   $a[1] = 2;
   $a[2] = 3;
   $a[3] = 5;
   $a[4] = 7;
   $a[5] = 11;
   
   // Faster way
   $a = [1 => 2, 
         2 => 3,
         3 => 5,
         4 => 7,
         5 => 11];
   
   // Even faster way if indexing is implicit
   $a = [2, 3, 5, 7, 11];
   
   ?>
Connex PHP features
-------------------

  + `preprocess <https://php-dictionary.readthedocs.io/en/latest/dictionary/preprocess.ini.html>`_


Suggestions
___________

* Preprocess the code so PHP doesn't do it at execution time. Keep the detailed version into comments.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/ShouldPreprocess                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


