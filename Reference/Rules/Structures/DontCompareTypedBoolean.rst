.. _structures-dontcomparetypedboolean:

.. _avoid-compare-typed-boolean:

Avoid Compare Typed Boolean
+++++++++++++++++++++++++++

  There is no need to compare explicitly a function call to a boolean, when the definition has a boolean return type.

The analysis checks for equality and identity comparisons. It doesn't check for the not operator usage.

.. code-block:: php
   
   <?php
   
   // Sufficient check
   if (foo()) {
       doSomething();
   }
   
   // Superfluous check
   if (foo() === true) {
       doSomething();
   }
   
   function foo() : bool {}
   
   ?>

Suggestions
___________

* Simplify the code and make it short




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontCompareTypedBoolean                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


