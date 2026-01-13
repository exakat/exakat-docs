.. _typehints-wrongtypewithdefault:

.. _wrong-type-with-default:

Wrong Type With Default
+++++++++++++++++++++++

  The default value is not of the declared type. 

For properties, this will generate an `error <https://www.php.net/error>`_ as soon as the default value is used : this is before constructor call for properties, and when the argument is omitted for promoted properties.

For parameters, the `error <https://www.php.net/error>`_ happens when the argument is omitted, and the default value is fetched. Otherwise, it won't happen. 
This `error <https://www.php.net/error>`_ is immediately detected when a literal value is used. It only happens when the default is a constant (class or global) or an expression, as those are only solved at execution time.

.. code-block:: php
   
   <?php
   
   const A = 1;
   
   class B {
       private string $c = A;
   }
   
   new B;
   //Cannot assign string to property B::$c of type string
   ?>

See also `When does PHP check for Fatal error <https://www.exakat.io/en/when-does-php-check-for-fatal-error/>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+assign+string+to+property+A%3A%3A%24g+of+type+int.html>`_




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/WrongTypeWithDefault                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.4                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


