.. _structures-multipletypevariable:

.. _multiple-type-variable:

Multiple Type Variable
++++++++++++++++++++++

  Avoid using the same variable with different types of data. 

It is recommended to use different names for differently typed data, while processing them. This prevents errors where one believe the variable holds the former type, while it has already been cast to the later.

Incrementing variables, with math operations or concatenation, is OK : the content changes, but not the type. And casting the variable without storing it in itself is OK.

.. code-block:: php
   
   <?php
   
   // $x is an array
   $x = range('a', 'z');
   // $x is now a string
   $x = join('', $x);
   $c = count($x); // $x is not an array anymore
   
   
   // $letters is an array
   $letters = range('a', 'z');
   // $alphabet is a string
   $alphabet = join('', $letters);
   
   // Here, $letters is cast by PHP, but the variable is changed.
   if ($letters) { 
       $count = count($letters); // $letters is still an array 
   }
   
   ?>

Suggestions
___________

* Use a class that accepts one type of argument, and exports another type of argument.
* Use different variable for each type of data format : $rows (for array), $list (for implode('', $rows))
* Pass the final result as argument to another method, avoiding the temporary variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleTypeVariable                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.15                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | variable, type                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-structures-multipletypevariable`, :ref:`case-vanilla-structures-multipletypevariable`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


