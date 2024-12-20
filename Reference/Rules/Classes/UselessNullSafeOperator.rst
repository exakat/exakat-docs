.. _classes-uselessnullsafeoperator:

.. _useless-nullsafe-operator:

Useless NullSafe Operator
+++++++++++++++++++++++++

  Nullsafe operator ``?->`` has no object when the types are never null, or when coalesce is active.

The nullsafe operator protects the execution from accessing a method or a property on a null value. If the object part of the syntax cannot be null, then the nullsafe operator ``?->`` will not protect it. 

The nullsafe operator is filling the same duty as ``??`` operator, although with a more granular precision. 


.. code-block:: php
   
   <?php
   
   function foo() : A {
   	return new A(); // or other code
   }
   
   // foo() always returns A, so it is always valid
   foo()?->methodOnA();
   
   // goo() may return NULL: ?-> and ?? are filling the same duty
   goo()?->methodOnA ?? C;
   
   function goo() : ?A {}
   
   ?>
Connex PHP features
-------------------

  + `nullsafe-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullsafe-operator.ini.html>`_


Suggestions
___________

* Replace the null safe operator with the normal one.
* Add the type null to the type declaration.
* Check for null-coalesce operator ?? and choose the most appropriate.




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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


