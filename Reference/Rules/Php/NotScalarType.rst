.. _php-notscalartype:

.. _not-a-scalar-type:

Not A Scalar Type
+++++++++++++++++

  ``int`` is the actual PHP scalar type, not ``integer``. 

PHP 7 introduced several scalar types, in particular ``int``, ``bool``, ``string`` and ``float``. Those three types are easily mistaken with ``integer``, ``boolean``, ``real`` and ``double``. 

Unless those classes actually exists, PHP emits some strange `error <https://www.php.net/error>`_ messages.
Thanks to ``Benoit Viguier`` for the `original idea <https://twitter.com/b_viguier/status/940173951908700161>`__ for this analysis.

.. code-block:: php
   
   <?php
   
   // This expects a scalar of type 'integer'
   function foo(int $i) {}
   
   // This expects a object of class 'integer'
   function abr(integer $i) {}
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_ and `PHP RFC: Scalar Type Hints <https://wiki.php.net/rfc/scalar_type_hints>`_.


Suggestions
___________

* Do not use ``int`` as a class name, an interface name or a trait name.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NotScalarType                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.7                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | scalar-typehint                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


