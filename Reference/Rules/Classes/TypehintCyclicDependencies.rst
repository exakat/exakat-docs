.. _classes-typehintcyclicdependencies:

.. _di-cyclic-dependencies:

DI Cyclic Dependencies
++++++++++++++++++++++

  When injecting dependencies, classes that mutually depend on each other is a code smell. 

Dependency injection should be organized as an acyclic tree-like structure

.. code-block:: php
   
   <?php
   
   // Classes A and B depends on each other. 
   class A {
       protected $b;
   
       public function __construct(B $b) {
           $this->b = $b;
       }
   }
   
   class B {
       public $a;
   
       protected function setA(A $a) {
           $this->a = $a;
       }
   }
   ?>

See also `Dependency Injection Smells <http://seregazhuk.github.io/2017/05/04/di-smells/>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TypehintCyclicDependencies                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | injection                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


