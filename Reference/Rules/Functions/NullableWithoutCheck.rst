.. _functions-nullablewithoutcheck:

.. _nullable-without-check:

Nullable Without Check
++++++++++++++++++++++

  Nullable typed argument or properties should be checked before usage. When they are null, they probably won't behave like the other type, and lead to an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // This will emit a fatal error when $a = null
   function foo(?A $a) {
       return $a->m();
   }
   
   // This is stable
   function foo(?A $a) {
       if ($a === null) {
           return 42;
       } else {
           return $a->m();
       }
   }
   
   ?>

See also `Null Return Types <https://afilina.com/learn/nulls/return-types>`_.


Suggestions
___________

* Add a check on return value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NullableWithoutCheck                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | null, return-typehint                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


