.. _functions-retypedreference:

.. _retyped-reference:

Retyped Reference
+++++++++++++++++

  A parameter with a reference may be typed differently, at the end of a method call. 

It is possible for a referenced and typed parameter to be retyped during a method call. As such, the type of the used variable might both be checked and changed. 

Using such syntax will lead to confusion in the code.
This works on all types, scalars or objects. 

This rule will detect variables which are defined with a placeholder value, or even undefined, and are filled during the method call.

.. code-block:: php
   
   <?php
   
   $a = [1];
   foo($a);
   echo $a; // Now, $a is a string
   
   function foo(array &$a) {
       $a = "Now, I am a string";
   }
   
   ?>

Suggestions
___________

* Do not change a referenced variable's type
* Set the called value to a compatible type.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/RetypedReference                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


