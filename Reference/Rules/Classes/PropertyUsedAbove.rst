.. _classes-propertyusedabove:

.. _property-used-above:

Property Used Above
+++++++++++++++++++

  Property used in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes. If the definition of the property is in the child class, then the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ should not know about it and make usage of it.

It may also be used in the current class, or its children, though this is not reported by this analyzer.


.. code-block:: php
   
   <?php
   
   class A {
       public function foo() {
           $this->pb++;
       }
   }
   
   class B extends A {
       protected $pb = 0;       // property     used above
       protected $pb2 = 0;      // property NOT used above
   }
   
   ?>

See also :ref:`Property Used Below <property-used-below>`.


Suggestions
___________

* Move the definition of the property to the upper class
* Move the usage of the property to the lower class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedAbove                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | property, inheritance                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


