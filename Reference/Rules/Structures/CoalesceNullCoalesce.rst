.. _structures-coalescenullcoalesce:

.. _coalesce-and-ternary-operators-order:

Coalesce And Ternary Operators Order
++++++++++++++++++++++++++++++++++++

  The ternary operator and the null-coalesce operator cannot be used in any order. The ternary operator is wider, so ot should be used last.

In particular, the ternary operator works on truthy values, and `NULL <https://www.php.net/manual/en/language.types.null.php>`_ is a falsy one. So, `NULL <https://www.php.net/manual/en/language.types.null.php>`_ might be captured by the ternary operator, and the following coalesce operator has no chance to process it. 

On the other hand, the coalesce operator only process `NULL <https://www.php.net/manual/en/language.types.null.php>`_, and will leave the false (or any other falsy value) to process to the ternary operator.


.. code-block:: php
   
   <?php
   
   // Good order : NULL is processed first, otherwise, false will be processed. 
   $b = $a ?? 'B' ?: 'C';
   
   // Wrong order : this will never use the ??
   $b = $a ?: 'C' ?? 'B';
   
   ?>

Suggestions
___________

* Use the good order of operator : most specific first, then less specific.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CoalesceNullCoalesce                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | ternary, null, coalesce                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


