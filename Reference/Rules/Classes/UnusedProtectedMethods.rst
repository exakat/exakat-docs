.. _classes-unusedprotectedmethods:

.. _unused-protected-methods:

Unused Protected Methods
++++++++++++++++++++++++

  The following protected methods are unused in children class. As such, they may be considered for being private.

Methods reported by this analysis are not used by children, yet they are protected.


.. code-block:: php
   
   <?php
   
   class Foo {
       // This method is not used
       protected function unusedBar() {}
       protected function usedInFoo() {}
       protected function usedInFooFoo() {}
       
       public function bar2() {
           // some code
           $this->usedInFoo();
       }
   }
   
   class FooFoo extends Foo {
       protected function bar() {}
       
       public function bar2() {
           // some code
           $this->usedInFooFoo();
       }
   }
   
   class someOtherClass {
       protected function bar() {
           // This is not related to foo.
           $this->unusedbar();
       }
   }
   
   ?>


No usage of those methods were found. 

This analysis is impacted by dynamic method calls.

Suggestions
___________

* Make use of the protected method in the code
* Remove the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedProtectedMethods                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | unused                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`unused-public-methods`                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


