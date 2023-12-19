.. _php-assumptions:

.. _assumptions:

Assumptions
+++++++++++

  Assumptions in the code, that leads to possible bugs. 

Some conditions may be very weak, and lead to errors. For example, the code below checks that the variable `$a` is not null, then uses it as an array. There is no relationship between 'not null' and 'being an array', so this is an assumption. 


.. code-block:: php
   
   <?php
   
   // Assumption : if $a is not null, then it is an array. This is not always the case. 
   function foo($a) {
       if ($a !== null) {
           echo $a['name'];
       }
   }
   
   // Assumption : if $a is not null, then it is an array. Here, the typehint will ensure that it is the case. 
   // Although, a more readable test is is_array()
   function foo(?array $a) {
       if ($a !== null) {
           echo $a['name'];
       }
   }
   
   ?>

See also `From assumptions to assertions <https://rskuipers.com/entry/from-assumptions-to-assertions>`_.


Suggestions
___________

* Make the context of the code more explicit
* Use a class to handle specific array index
* Avoid using named index by using foreach()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Assumptions                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | assumption                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


