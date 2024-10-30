.. _structures-couldusenullableoperator:

.. _could-use-null-safe-object-operator:

Could Use Null-Safe Object Operator
+++++++++++++++++++++++++++++++++++

  When the preceding function call has the potential to return null, employing the null-safe object operator can help mitigate fatal errors.

One approach is to assess the returned value prior to utilization, ensuring it is not null, and refraining from invoking methods on a null reference. Alternatively, the null-safe operator can be employed, allowing verification of the end `result <https://www.php.net/result>`_. If the `result <https://www.php.net/result>`_ is null, it indicates an `error <https://www.php.net/error>`_.

Another approach is to use the null-safe operator when the intermediate methods returns an object or a null. When chained, the null-safe operator will prevent Fatal `Error <https://www.php.net/error>`_. 


.. code-block:: php
   
   <?php
   
   // direct usage, with a check on the final value
   $a = foo()?->b() ?? throw new exception('something went wrong when calculating $a');
      // throw as an expression is a PHP 8.0 code
   
   
   // direct usage, may yield a Fatal error
   foo()->b();
   
   // indirect usage, with a check on the returned value
   $a = foo();
   $c = $a ? $a->b() : null;
   
   
   function foo() : ?A {
       return rand(0, 1) ? new A() : null;
   }
   
   class A {
       function b() : string { return '';}
   }
   
   ?>

See also `PHP 8.0 feature focus: nullsafe methods <https://platform.sh/blog/2020/php-80-feature-focus-type-nullsafe-methods/>`_ and `Nullsafe methods and properties <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.nullsafe>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Call+to+a+member+function+b%28%29+on+null.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Attempt+to+read+property+%22b%22+on+null.html>`_
  + `2 <https://php-errors.readthedocs.io/en/latest/messages/Class+%22null%22+not+found+.html>`_



Connex PHP features
-------------------

  + `nullsafe-object-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullsafe-object-operator.ini.html>`_
  + `nullable <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullable.ini.html>`_


Suggestions
___________

* Add a check on NULL before using the returned value
* Update the previous method to prevent it from returning null
* Use the null-safe object operator and test the result afterward




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseNullableOperator                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


