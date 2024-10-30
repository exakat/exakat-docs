.. _classes-propertyusedbelow:

.. _property-used-below:

Property Used Below
+++++++++++++++++++

  This rule marks properties that are used in children classes.

This analysis doesn't mark the current class, nor the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or grand `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes.

.. code-block:: php
   
   <?php
   
   class foo {
       // This property is used in children
       protected protectedProperty = 1;
       
       // This property is not used in children
       protected localProtectedProperty = 1;
   
       private function foobar() {
           // protectedProperty is used here, but defined in parent
           $this->localProtectedProperty = 3;
       }
   }
   
   class foofoo extends foo {
       private function bar() {
           // protectedProperty is used here, but defined in parent
           $this->protectedProperty = 3;
       }
   }
   
   ?>

See also :ref:`Property Used Above <property-used-above>`.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedBelow                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


