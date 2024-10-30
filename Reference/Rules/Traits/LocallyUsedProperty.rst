.. _traits-locallyusedproperty:

.. _locally-used-property-in-trait:

Locally Used Property In Trait
++++++++++++++++++++++++++++++

  List of properties that are used in the trait where they are defined. A property should be used at least once in the trait of its definition.

.. code-block:: php
   
   <?php
   
   trait foo {
       public $unused, $used;// property $unused is never used in this trait
       
       function bar() {
           $this->used++; // property $used is used in this method
       }
   }
   
   class X {
       use foo;
   }
   
   $foo = new X();
   $foo->unused = 'here'; // property $unused is used outside the trait definition
   ?>
Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/LocallyUsedProperty                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


