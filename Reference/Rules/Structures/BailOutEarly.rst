.. _structures-bailoutearly:

.. _bail-out-early:

Bail Out Early
++++++++++++++

  When using conditions, it is recommended to quit in the current context, and avoid the else clause altogether. 

The main benefit is to make clear the method applies a condition, and stop immediately when this condition is not satisfied. 
The main sequence is then focused on the important code. 

This analysis works with the ``break``, ``continue``, ``throw`` and ``goto`` keywords too, depending on situations.


.. code-block:: php
   
   <?php
   
   // Bailing out early, low level of indentation
   function foo1($a) {
       if ($a > 0) {
           return false;
       } 
       
       $a++;
       return $a;
   }
   
   // Works with continue too
   foreach($array as $a => $b) {
       if ($a > 0) {
           continue false;
       } 
       
       $a++;
       return $a;
   }
   
   // No need for else
   function foo2($a) {
       if ($a > 0) {
           return false;
       } else {
           $a++;
       }
       
       return $a;
   }
   
   // No need for else : return goes into then. 
   function foo3($a) {
       if ($a < 0) {
           $a++;
       } else {
           return false;
       }
       
       return $a;
   }
   
   // Make a return early, and make the condition visible.
   function foo3($a) {
       if ($a < 0) {
           $a++;
           methodcall();
           functioncall();
       } 
   }
   
   ?>

See also `Avoid nesting too deeply and return early (part 1) <https://github.com/jupeter/clean-code-php#avoid-nesting-too-deeply-and-return-early-part-1>`_ and `Avoid nesting too deeply and return early (part 2) <https://github.com/jupeter/clean-code-php#avoid-nesting-too-deeply-and-return-early-part-2>`_.


Suggestions
___________

* Detect errors, and then, return as soon as possible.
* When a if...then branches are unbalanced, test for the small branch, finish it with return. Then keep the other branch as the main code.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BailOutEarly                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | return                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-structures-bailoutearly`, :ref:`case-opencfp-structures-bailoutearly`                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


