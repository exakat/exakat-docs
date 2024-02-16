.. _classes-hiddennullable:

.. _hidden-nullable-typehint:

Hidden Nullable Typehint
++++++++++++++++++++++++

  Argument with default value of null are nullable. It works both with the ``null`` typehint (PHP 8.0), or the ``?`` operator are not used, setting the default value to null is allowed, and makes the argument nullable.

This works with single types, both classes and scalars; it works with union types but not with intersection types. 

This doesn't happen with properties : they must be defined with the nullable type to accept a ``null``value as default value.

This doesn't happen with constant, which can't be typehinted. 


.. code-block:: php
   
   <?php
   
   // explicit nullable parameter $s
   function bar(?string $s = null) {
   
   // implicit nullable parameter $s
   function foo(string $s = null) {
       echo $s ?? 'NULL-value';
   }
   
   // both display NULL-value
   foo(); 
   foo(null);
   
   ?>

See also `Nullable types <https://wiki.php.net/rfc/nullable_types>`_, `Type declaration <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_ and `Deprecate implicit nullable parameters #3535 <https://github.com/php/php-src/pull/3535>`_.


Suggestions
___________

* Change the default value to a compatible literal : for example, ``string $s = ''``
* Add the explicit ``?`` nullable operator, or ``null``with PHP 8.0
* Remove the default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/HiddenNullable                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint, nullable                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


