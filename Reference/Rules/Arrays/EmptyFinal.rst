.. _arrays-emptyfinal:

.. _empty-final-element-in-array:

Empty Final Element In Array
++++++++++++++++++++++++++++

  The `array() <https://www.php.net/array>`_ construct allows for the empty last element. 

By putting an element on each line, and adding the final comma, it is possible to reduce the size of the diff when comparing code with the previous version.

.. code-block:: php
   
   <?php
   
   // Array definition with final empty element
   $array = [1,
             2,
             3,
             ];
   
   // New version of the code above
   // This array definition has only one line of diff with the previous array : the line with '4,'
   $array = [1,
             2,
             3,
             4,
             ];
   
   // New version of the first code above
   // This array definition is totally different from the first array : VCS will identify 3 removed lines, and one modified.
   $array = [1, 2, 3, 4];
   
   ?>

See also `Array <https://www.php.net/manual/en/language.types.array.php>`_, `Zend Framework Coding Standard <https://framework.zend.com/manual/2.4/en/ref/coding.standard.html#arrays>`_ and `How clean is your code? How clean are your diffs? <https://blog.madewithlove.be/post/code-style-options-for-cleaner-diffs/>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/EmptyFinal                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | trailing-comma                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


