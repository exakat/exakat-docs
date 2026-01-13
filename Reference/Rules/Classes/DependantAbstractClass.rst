.. _classes-dependantabstractclass:

.. _dependant-abstract-classes:

Dependant Abstract Classes
++++++++++++++++++++++++++

  Abstract classes should be autonomous. It is recommended to avoid depending on methods, constant or properties that should be made available in inheriting classes, without explicitly abstracting them.

The following abstract classes make usage of constant, methods and properties, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not, that are not defined in the class. This means the inheriting classes must provide those constants, methods and properties, but there is no way to enforce this. 

This may also lead to dead code : when the abstract class is removed, the host class have unused properties and methods.

.. code-block:: php
   
   <?php
   
   // autonomous abstract class : all it needs is within the class
   abstract class c {
       private $p = 0;
       
       function foo() {
           return ++$this->p;
       }
   }
   
   // dependant abstract class : the inheriting classes needs to provide some properties or methods
   abstract class c2 {
       function foo() {
           // $p must be provided by the extending class
           return ++$this->p;
       }
   }
   
   class c3 extends c2 {
       private $p = 0;
   }
   ?>

See also :ref:`Dependant Trait <dependant-trait>`.

Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Make the class only use its own resources
* Split the class in autonomous classes
* Add local property definitions to make the class independent




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DependantAbstractClass                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.6                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


