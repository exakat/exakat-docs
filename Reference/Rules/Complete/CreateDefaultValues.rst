.. _complete-createdefaultvalues:

.. _create-default-values:

Create Default Values
+++++++++++++++++++++

  This commands adds a link between variables, property definitions and any assignation to this container.

Variables have no definition expression in PHP. Exakat holds their definition with the `Variabledefinition` node.

Properties have definitions, and non-compulsory default values. This command creates multiple DEFINITION link for them.

DEFAULT is convenient in the case of `null` value, which will be assigned an object at execution time. 


.. code-block:: php
   
   <?php
   
   function foo() {
       // local Variabledefinition links to this expression
       $a = 1;
   }
   
   class x {
       // 1 is a default value
       private $p = 1;
       
       function __construct() {
           // 2 is also a default value for this.
           // This default value is different from the above as it is a part of an assignation
           $this->p = 2;
       }
   }
   
   ?>


Short assignations, such as `+=`  are not considered default value. It needs to be a full assignation

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateDefaultValues                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


