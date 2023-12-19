.. _functions-mismatchedtypehint:

.. _mismatched-typehint:

Mismatched Typehint
+++++++++++++++++++

  Relayed arguments don't have the same typehint.

Typehint acts as a filter method. When an object is checked with a first class, and then checked again with a second distinct class, the whole process is always false : $a can't be of two different classes at the same time.


.. code-block:: php
   
   <?php
   
   // Foo() calls bar()
   function foo(A $a, B $b) {
       bar($a, $b);
   }
   
   // $a is of A typehint in both methods, but 
   // $b is of B then BB typehing
   function bar(A $a, BB $b) {
   
   }
   
   ?>


Note : This analysis currently doesn't check generalisation of classes : for example, when B is a child of BB, it is still reported as a mismatch.

Suggestions
___________

* Ensure that the default value match the expected typehint.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchedTypehint                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Typechecks <ruleset-Typechecks>`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.3                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-functions-mismatchedtypehint`                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


