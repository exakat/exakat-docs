.. _traits-unusedclasstrait:

.. _unused-trait-in-class:

Unused Trait In Class
+++++++++++++++++++++

  A trait has been summoned in a class, but is not used. Traits may be used as a copy/paste of code, bringing a batch of methods and properties to a class. In the current case, the imported trait is never called. As such, it may be removed. 

Currently, the analysis covers only traits that are used in the class where they are imported. Also, the properties are not covered yet. 



There are some sneaky situations, where a trait falls into decay : for example, creating a method in the importing class, with the name of a trait class, will exclude the trait method, as the class method has priority. Other precedence rules may lead to the same effect.

.. code-block:: php
   
   <?php
   
   trait t {
       function foo() { return 1;}
   }
   
   // this class imports and uses the trait
   class UsingTrait {
       use t;
       
       function bar() {
           return $this->foo() + 1;
       }
   }
   
   // this class imports but doesn't uses the trait
   class UsingTrait {
       use t;
       
       function bar() {
           return 1;
       }
   }
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.


Suggestions
___________

* Remove the trait from the class
* Actually use the trait, at least in the importing class
* Use conflict resolution to make the trait accessible




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UnusedClassTrait                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | trait                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


