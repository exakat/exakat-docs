.. _functions-toomuchindented:

.. _too-much-indented:

Too Much Indented
+++++++++++++++++

  Reports methods that are using more than one level of indentation on average. 

Indentations levels are counted for each for, foreach, if...then, while, do..while, try..catch..finally structure met. Compulsory expressions, such as conditions, are not counted in the total. Levels of indentation start at 0 (no indentation needed)

This analysis targets methods which are build around large conditions : the actual useful code is nested inside the branches of the if/then/else (for example). 

The default threshold ``indentationAverage`` of 1 is a good start for spotting large methods with big conditional code, and will leave smaller methods, even when they only contain one if/then. Larger methods shall be refactored in smaller size. 

The parameter ``minimumSize`` set aside methods which are too small for refactoring.
This analysis is distinct from Structures/MaxLevelOfIdentation, which only reports the highest level of indentation. This one reports how one method is build around one big

.. code-block:: php
   
   <?php
   
   // average 0
   function foo0() {
       $a = rand(1,2);
       $a *= 3;
       
       return $a;
   }
   
   // average 0.66 = (0 + 1 + 1) / 3
   function foo0_66() {
       // if () is at level 0
       if ($a == 2) { // condition is not counted
           $a = 1;    // level 1
       } else {
           $a = 2;    // level 1
       }
   }
   
   // average 1 = (0 + 2 + 1 + 1) / 4
   function foo1() {
       // if () is at level 0
       if ($a == 2) {
           // if () is at level 1
           if ($a == 2) {
               $a = 1; // level 2
           }
           $a = 1; // level 1
       } else {
           $a = 2; // level 1
       }
   }
   
   ?>

+--------------------+---------+------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Name               | Default | Type | Description                                                                                                                                          |
+--------------------+---------+------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| indentationAverage | 1       | real | Minimal average of indentation in a method to report. Default is 1.0, which means that the method is on average at one level of indentation or more. |
+--------------------+---------+------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| minimumSize        | 3       | real | Minimal number of expressions in a method to apply this analysis.                                                                                    |
+--------------------+---------+------+------------------------------------------------------------------------------------------------------------------------------------------------------+



See also :ref:`Max Level Of Nesting <max-level-of-nesting>`.

Connex PHP features
-------------------

  + `indentation <https://php-dictionary.readthedocs.io/en/latest/dictionary/indentation.ini.html>`_


Suggestions
___________

* Refactor the method to reduce the highest level of indentation
* Refactor the method move some of the code to external methods.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TooMuchIndented                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


