.. _classes-noreadonlyassignationinglobal:

.. _no-readonly-assignation-in-global:

No Readonly Assignation In Global
+++++++++++++++++++++++++++++++++

  When a property is marked readonly, it may only be assigned within the class of definition.

It cannot be assigned outside this class, in the global scope. It is also immune to class invasion.

.. code-block:: php
   
   <?php
   
   class x {
       public readonly int $p;
       
       function foo() {
           $this->p -= 1; // OK
           
           $x = new x;
           $x->p = 1;     // Not OK, even if $x is of type x
       }
   }
   
   $x = new x;
   $x->p = 1;     // Not OK
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoReadonlyAssignationInGlobal                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | readonly, class-invasion                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


