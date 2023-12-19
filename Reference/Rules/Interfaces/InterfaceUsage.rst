.. _interfaces-interfaceusage:

.. _interfaces-usage:

Interfaces Usage
++++++++++++++++

  List of used interfaces.

Interfaces are used when mentioned in a class or another interface, with implements keyword; they are used in `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ expression, in typehints and class constant.


.. code-block:: php
   
   <?php
   
   // interface definition
   interface i {
       const I = 2;
   }
   
   // interface extension 
   interface i2 extends i {}
   
   // interface implementation 
   class foo implements i {}
   
   $foo = new foo();
   
   var_dump($foo instanceof i);
   
   function bar( i $arg) { }
   bar($foo);
   
   // in class constant
   echo i::I;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/InterfaceUsage                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | interface                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


