.. _patterns-factory:

.. _an-oop-factory:

An OOP Factory
++++++++++++++

  A method or function that implements a factory. A factory is a class that handles the creation of an object, based on parameters. The factory hides the logic that leads to the creation of the object.

.. code-block:: php
   
   <?php
       class AutomobileFactory {
           public static function create($make, $model) {
               $className = "\Automaker\Brand$make";
               return new $className($model);
           }
       }
       
       // The factory is able to build any car, based on their 
       $fuego = AutomobileFactory::create('Renault', 'Fuego');
       
       print_r($fuego->getMakeAndModel()); // outputs "Renault Fuego" 
   ?>

See also `Factory (object-oriented programming) <https://en.wikipedia.org/wiki/Factory_(object-oriented_programming)>`_ and `Factory <https://phptherightway.com/pages/Design-Patterns.html#factory>`_.

Connex PHP features
-------------------

  + `pattern <https://php-dictionary.readthedocs.io/en/latest/dictionary/pattern.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/Factory                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


