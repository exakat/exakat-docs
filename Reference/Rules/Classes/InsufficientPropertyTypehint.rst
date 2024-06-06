.. _classes-insufficientpropertytypehint:

.. _insufficient-property-typehint:

Insufficient Property Typehint
++++++++++++++++++++++++++++++

  The typehint used for a class property doesn't cover all it usage.

The typehint is insufficient when a undefined method or constant is called, or if members are accessed while the typehint is an interface.
This analysis relies on typehinted properties, as introduced in PHP 7.4. It also relies on typehinted assignations at construct time : the typehint of the assigned argument will be used as the property typehint. Getters and setters are not considered here.

.. code-block:: php
   
   <?php
   
   class A {
       function a1() {}
   }
   
   // PHP 7.4 and more recent
   class B {
       private A $a = null;
       
       function b2() {
           // this method is available in A
           $this->a->a1();
           // this method is NOT available in A
           $this->a->a2();
       }
   }
   
   // Supported by all PHP versions
   class C {
       private $a = null;
   
       function __construct(A $a) {
           $this->a = $a;
       }
       
       function b2() {
           // this method is available in A
           $this->a->a1();
           // this method is NOT available in A
           $this->a->a2();
       }
   }
   
   ?>

Suggestions
___________

* Change the typehint to match the actual usage of the object in the class. 




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/InsufficientPropertyTypehint                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


