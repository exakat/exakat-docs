.. _classes-nonullwithnullsafeoperator:

.. _no-null-with-null-safe-operator:

No Null With Null Safe Operator
+++++++++++++++++++++++++++++++

  When building an expression with a null-safe operator, it may fail and produce a `NULL <https://www.php.net/manual/en/language.types.null.php>`_ as a `result <https://www.php.net/result>`_. When the last method of the expression also returns null (or void, which is transformed in null), then it is not possible to differentiate between a failure and a valid execution of the method. 

As such, it is recommended to avoid finishing with a method that returns null, in an expression that uses a null-safe operator.


.. code-block:: php
   
   <?php
   
   class x {
   	function foo($a) : ?int { 
   		if ($a % 2) {
   			return $a;
   		} else {
   			return null;
   		}
   	}
   }
   
   $x = x::getInstance(x::class);
   $result = $x?->foo($a);
   
   // Is that an error or a valid result ? 
   if ($result === null) { }
   
   ?>

Suggestions
___________

* Avoid using the null-safe operator in that expression
* Make the last property / method in the expression not return null




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoNullWithNullSafeOperator                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------+
| PHP Version  | 8.1                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------+
| Features     | null-safe-operator                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------+
| Available in |                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------+


