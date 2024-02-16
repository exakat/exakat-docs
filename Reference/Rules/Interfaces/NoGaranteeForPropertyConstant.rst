.. _interfaces-nogaranteeforpropertyconstant:

.. _interfaces-don't-ensure-properties:

Interfaces Don't Ensure Properties
++++++++++++++++++++++++++++++++++

  When using an interface as a type, properties are not enforced, nor available.

An interface is a template for a class, which specify the minimum amount of methods and constants. Properties are never defined in an interface, and should not be relied upon.


.. code-block:: php
   
   <?php
   
   interface i {
       function m () ;
   }
   
   class x implements i {
       public $p = 1;
       
       function m() {
           return $this->p;
       }
   }
   
   function foo(i $i, x $x) {
       // this is invalid, as $p is not defined in i, so it may be not available
       echo $i->p;
       
       // this is valid, as $p is defined in $x
       echo $x->p;
   }
   
   ?>

See also `Interface And Abstract Class <https://medium.com/@atakde/interface-and-abstract-class-6f5cae27fa07>`_.


Suggestions
___________

* Use classes for type when properties are accessed
* Only use methods and constants which are available in the interface
* Use an abstract class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/NoGaranteeForPropertyConstant                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | interface                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


