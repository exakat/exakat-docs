.. _php-cantusereturnvalueinwritecontext:

.. _cant-use-return-value-in-write-context:

Cant Use Return Value In Write Context
++++++++++++++++++++++++++++++++++++++

  empty() used to work only on data containers, such as variables. Until PHP 5.5, it was not possible to use directly expressions, such as functioncalls, inside an empty() function call : they were met with a 'Can't use function return value in write context' fatal `error <https://www.php.net/error>`_. 


.. code-block:: php
   
   <?php
   
   function foo($boolean) {
       return $boolean;
   }
   
   // Valid since PHP 5.5
   echo empty(foo(true)) : 'true' : 'false';
   
   ?>


This also applies to methodcalls, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not.

See also `Cant Use Return Value In Write Context <https://stackoverflow.com/questions/1075534/cant-use-method-return-value-in-write-context>`_.


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CantUseReturnValueInWriteContext                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | return                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


