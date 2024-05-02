.. _structures-oneifissufficient:

.. _one-if-is-sufficient:

One If Is Sufficient
++++++++++++++++++++

  Nested conditions may be rewritten another way, to reduce the amount of code.

Nested conditions are equivalent to an ``&&`` condition. As such, they may be switched. When one of the condition has no explicit else, then it is lighter to write it as the first condition. This way, it is written once, and not repeated.

.. code-block:: php
   
   <?php
   
   // Less conditions are written here.
       if($b == 2) {
           if($a == 1) {
               ++$c;
           }
           else {
               ++$d;
           }
       }
   
   // ($b == 2) is double here
       if($a == 1) {
           if($b == 2) {
               ++$c;
           }
       }
       else {
           if($b == 2) {
               ++$d;
           }
       }
   ?>

Suggestions
___________

* Switch the if...then conditions, to reduce the amount of conditions to read. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneIfIsSufficient                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tikiwiki-structures-oneifissufficient`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


