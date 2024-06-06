.. _classes-constantusedbelow:

.. _constant-used-below:

Constant Used Below
+++++++++++++++++++

  Mark class constants that are used in children classes.
This analysis marks constants at their definition, not the current class, nor the (grand-)`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

.. code-block:: php
   
   <?php
   
   class foo {
       // This constant is used in children
       protected PROTECTEDPROPERTY = 1;
       
       // This constant is not used in children
       protected LOCALPROTECTEDPROPERTY = 1;
   
       private function foobar() {
           // PROTECTEDPROPERTY is used here, but defined in parent
           echo self::LOCALPROTECTEDPROPERTY;
       }
   }
   
   class foofoo extends foo {
       private function bar() {
           // protectedProperty is used here, but defined in parent
           print self::PROTECTEDPROPERTY;
       }
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ConstantUsedBelow                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.10                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class-constant                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


