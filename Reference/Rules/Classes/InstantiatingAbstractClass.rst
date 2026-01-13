.. _classes-instantiatingabstractclass:

.. _instantiating-abstract-class:

Instantiating Abstract Class
++++++++++++++++++++++++++++

  PHP cannot instantiate an abstract class. 

The classes are actually abstract classes, and should be derived into a concrete class to be instantiated.

.. code-block:: php
   
   <?php
   
   abstract class Foo {
       protected $a;
   }
   
   class Bar extends Foo {
       protected $b;
   }
   
   // instantiating a concrete class.
   new Bar();
   
   // instantiating an abstract class.
   // In real life, this is not possible also because the definition and the instantiation are in the same file
   new Foo();
   
   ?>

See also `Class Abstraction <https://www.php.net/abstract>`_.

Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_
  + `concrete <https://php-dictionary.readthedocs.io/en/latest/dictionary/concrete.ini.html>`_


Suggestions
___________

* Make the class non abstract
* Extends that class with a new class that is not abstract. Instantiate that second class.
* Find an existing concrete class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/InstantiatingAbstractClass                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


