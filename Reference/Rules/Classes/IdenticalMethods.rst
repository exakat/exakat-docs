.. _classes-identicalmethods:

.. _identical-methods:

Identical Methods
+++++++++++++++++

  When the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class and the child class have the same method, the child might omit it. This reduces code duplication. 

Duplicate code in methods is often the results of code evolution, where a method was copied with the hierarchy, but the original wasn't removed.

This doesn't apply to `private` methods, which are reserved for one class.

.. code-block:: php
   
   <?php
   
   class a {
       public function foo() {
           return rand(0, 100);
       }
   }
   
   class b extends a {
       public function foo() {
           return rand(0, 100);
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Drop the method from the parent class, in particular if only one child uses the method.
* Drop the method from the child class, in particular if there are several children class
* Use an abstract method, and make sure every child has its own implementation
* Modify one of the methods so they are different




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IdenticalMethods                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


