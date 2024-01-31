.. _classes-uselessnullsafeoperator:

.. _useless-nullsafe-operator:

Useless NullSafe Operator
+++++++++++++++++++++++++

  The nullsafe operator protects the code from accessing a method or a property on a null value. If the object part of the syntax cannot be null, then the nullsafe operator ``?->`` will not protect it. 

.. code-block:: php
   
   <?php
   
   function foo() : A {
   	return new A(); // or other code
   }
   
   // foo() always returns A, so it is always valid
   foo()?->methodOnA();
   
   
   ?>

Suggestions
___________

* Replace the null safe operator with the normal one.
* Add the type null to the type declaration.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessNullSafeOperator                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | nullsafe-operator                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


