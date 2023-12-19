.. _classes-coulduseclassoperator:

.. _could-use-class-operator:

Could Use Class Operator
++++++++++++++++++++++++

  The class operator is `\:\:class`. With a class name as left operator, it provides the full class name. 

Classes may also be identified with a string, as a fully qualified name. Using the class operator is a more explicit way to do it.

The `\:\:class` operator works with the local use expressions. It also provides a string, which may be further processed.


.. code-block:: php
   
   <?php
   
   use A\B\C;
   
   $a = C::class;
   $a = \A\B\C::class; // also valid
   $object = new $a(); // object of A\B\C.
   
   // string version
   $a = '\a\b\c';
   $object = new $a(); // object of A\B\C.
   
   ?>


The class operator is also called the 'scope resolution operator'.

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.


Suggestions
___________

* Replace the string with the class operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldUseClassOperator                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class-operator                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


