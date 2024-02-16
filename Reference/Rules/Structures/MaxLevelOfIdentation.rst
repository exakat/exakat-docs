.. _structures-maxlevelofidentation:

.. _max-level-of-nesting:

Max Level Of Nesting
++++++++++++++++++++

  Avoid nesting structures too deep, as it hurts readability.

Nesting structures are : if/then, switch, for, foreach, while, do...while. Ternary operator, try/catch are not considered a nesting structures.

Closures, and more generally, functions definitions are counted separatedly. 

This analysis checks for 4 levels of nesting, by default. This may be changed by configuration.


.. code-block:: php
   
   <?php
   
   // 5 levels of indentation
   function foo() {
       if (1) {
           if (2) {
               if (3) {
                   if (4) {
                       if (5) {
                           51;
                       } else {
                           5;
                       }
                   } else {
                       4;
                   }
               } else {
                   3;
               }
           } else {
               2;
           }
       } else {
           1;
       }
   }
   
   // 2 levels of indentation
   function foo() {
       if (1) {
           if (2) {
               // 3 levels of indentation
               return function () {
                   if (3) {
                       if (4) {
                           if (5) {
                               51;
                           } else {
                               5;
                           }
                       } else {
                           4;
                       }
                   } else {
                       3;
                   }
               }
           } else {
               2;
           }
       } else {
           1;
       }
   }
   
   
   ?>

+----------+---------+---------+---------------------------------------------------------------------+
| Name     | Default | Type    | Description                                                         |
+----------+---------+---------+---------------------------------------------------------------------+
| maxLevel | 4       | integer | Maximum level of nesting for control flow structures in one scope.  |
+----------+---------+---------+---------------------------------------------------------------------+



See also `Indentation and Spacing in PHP <https://courses.cs.washington.edu/courses/cse154/17au/styleguide/php/spacing-indentation-php.html>`.


Suggestions
___________

* Refactor code to avoid nesting
* Export some nested blocks to an external method or function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MaxLevelOfIdentation                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | indentation                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


