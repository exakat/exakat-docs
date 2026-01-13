.. _traits-dependanttrait:

.. _dependant-trait:

Dependant Trait
+++++++++++++++

  Traits should be autonomous. It is recommended to avoid depending on methods or properties that should be in the using class.

The following traits make usage of methods and properties, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not, that are not defined in the trait. This means the host class must provide those methods and properties, but there is no way to enforce this. 

This may also lead to dead code : when the trait is removed, the host class have unused properties and methods.

.. code-block:: php
   
   <?php
   
   // autonomous trait : all it needs is within the trait
   trait t {
       private $p = 0;
       
       function foo() {
           return ++$this->p;
       }
   }
   
   // dependant trait : the host class needs to provide some properties or methods
   trait t2 {
       function foo() {
           return ++$this->p;
       }
   }
   
   class x {
       use t2;
       
       private $p = 0;
   }
   ?>

See also :ref:`Dependant Abstract Classes <dependant-abstract-classes>`.

Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Add local property definitions to make the trait independent
* Make the trait only use its own resources
* Split the trait in autonomous traits




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/DependantTrait                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-traits-dependanttrait`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


