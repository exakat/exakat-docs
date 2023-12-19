.. _interfaces-uselessinterfaces:

.. _useless-interfaces:

Useless Interfaces
++++++++++++++++++

  The interfaces below are defined and are implemented by some classes. 

However, they are never used to enforce an object's class in the code, using ``instanceof`` or in a type. 
As they are currently used, those interfaces may be removed without change in behavior.


.. code-block:: php
   
   <?php
       // only defined interface but never enforced
       interface i {};
       class c implements i {} 
   ?>


Interfaces should be used in type or with the ``instanceof`` operator. 


.. code-block:: php
   
   <?php
       interface i {};
       
       function foo(i $arg) { 
           // Now, $arg is always an 'i'
       }
       
       function bar($arg) { 
           if (!($arg instanceof i)) {
               // Now, $arg is always an 'i'
           }
       }
   ?>

Suggestions
___________

* Use the interface with instanceof, or a type
* Drop the interface altogether : both definition and implements keyword




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/UselessInterfaces                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | interface                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-interfaces <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-interfaces.md>`__                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-interfaces-uselessinterfaces`                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+


