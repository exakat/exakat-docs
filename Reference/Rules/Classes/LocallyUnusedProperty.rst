.. _classes-locallyunusedproperty:

.. _locally-unused-property:

Locally Unused Property
+++++++++++++++++++++++

  Those properties are defined in a class, and this class doesn't have any method that makes use of them. 

While this is syntactically correct, it is unusual that defined resources are used in a child class. It may be worth moving the definition to another class, or to move accessing methods to the class.

.. code-block:: php
   
   <?php
   
   class foo {
       public $unused, $used;// property $unused is never used in this class
       
       function bar() {
           $this->used++; // property $used is used in this method
       }
   }
   
   class foofoo extends foo {
       function bar() {
           $this->unused++; // property $unused is used in this method, but defined in the parent class
       }
   }
   
   ?>

Suggestions
___________

* Move the property definition to the child classes
* Move some of the child method, using the property, to the parent class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/LocallyUnusedProperty                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | property                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


