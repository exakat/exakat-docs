.. _typehints-couldbeiterable:

.. _typehint-could-be-iterable:

Typehint Could Be Iterable
++++++++++++++++++++++++++

  Mark arguments, class constants, properties and return types that can be set to ``iterable``.

.. code-block:: php
   
   <?php
   
   // Accept an array or a traversable Object as input 
   function foo($b) {
       foreach($b as $c) {
       
       }
   
       // Returns an array
       return [$b];
   }
   
   ?>
Connex PHP features
-------------------

  + `iterable <https://php-dictionary.readthedocs.io/en/latest/dictionary/iterable.ini.html>`_


Suggestions
___________

* Add `iterable` typehint to the code (PHP 8.0+).




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeIterable                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Typechecks <ruleset-Typechecks>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


