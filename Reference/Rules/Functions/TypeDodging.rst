.. _functions-typedodging:

.. _type-dodging:

Type Dodging
++++++++++++

  It is always possible to rewrite a parameter type by using union types. When the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class or interface requires a type, the child class may create a union type with the required type, add a secondary type and ignore the first one. 

This is part of the Liskov Substitution Principle, so the syntax is legit. When the union type is only used to circumvent the previous typing, it is now a violation, as such a typed data would be valid, but ignored.

.. code-block:: php
   
   <?php
   
   interface i {
   	function foo(A $a) {}
   }
   
   class x implement i {
   	function foo(A | string $a) {
   		if ($a instanceof A) {
   			throw new Exception('Unused type.');
   		}
   		// ...
   	}
   } 
   ?>

Suggestions
___________

* Avoid using union type to enlarge types in parameters




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TypeDodging                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | liskov                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


