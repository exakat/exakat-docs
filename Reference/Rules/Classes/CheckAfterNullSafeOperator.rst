.. _classes-checkafternullsafeoperator:

.. _check-after-null-safe-operator:

Check After Null Safe Operator
++++++++++++++++++++++++++++++

  Null-safe operator is ``?->``, which prevents fatal errors in case the object of the call is `NULL <https://www.php.net/manual/en/language.types.null.php>`_. The execution continues, though the `result <https://www.php.net/result>`_ of the expression is now `NULL <https://www.php.net/manual/en/language.types.null.php>`_ too. 

While it saves some checks in certain cases, the null-safe operator should be followed by a check on the returned value to process any misfire of the method. 

This analysis checks that the `result <https://www.php.net/result>`_ of the expression is collected, and compared to null.

.. code-block:: php
   
   <?php
   
   $result = $object?->foo(); 
   
   if ($result === null) {
   	throw new ObjectException(The object could not call $foo\n);
   }
   
   ?>

Suggestions
___________

* Collect and check the result of the expression to null
* Remove the null-safe operator and check before calling the object's method or property




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CheckAfterNullSafeOperator                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | nullsafe-object-operator                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


