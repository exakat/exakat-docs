.. _traits-methodcollisiontraits:

.. _method-collision-traits:

Method Collision Traits
+++++++++++++++++++++++

  Two or more traits are included in the same class, and they have methods collisions. 

Those collisions should be solved with a ``use`` expression. When they are not, PHP stops execution with a fatal `error <https://www.php.net/error>`_ : ``Trait method M has not been applied, because there are collisions with other trait methods on C``.


.. code-block:: php
   
   <?php
   
   trait A {
       public function A() {}
       public function M() {}
   }
   
   trait B {
       public function B() {}
       public function M() {}
   }
   
   class C {
       use  A, B;
   }
   
   class D {
       use  A, B{
           B::M insteadof A;
       };
   }
   
   ?>


The code above lints, but doesn't execute.

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.


Suggestions
___________

* method
* trait




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/MethodCollisionTraits                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | trait, method-collision                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


