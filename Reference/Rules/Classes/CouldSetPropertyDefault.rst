.. _classes-couldsetpropertydefault:

.. _could-set-property-default:

Could Set Property Default
++++++++++++++++++++++++++

  When a property is set to a literal in the constructor, the assignation may be moved to the property definition.


.. code-block:: php
   
   <?php
   
   class x {
       private $p;
       private $p2;
       
       function __construct($d) {
           // dynamic default value. 
           $this->p = $d;
   
           $this->p2 = "2";
       }
   
   }
   
   ?>


It is a micro-optimisation.

Suggestions
___________

* Set the default value to the property declaration, and remove the assignation in the constructor




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldSetPropertyDefault                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


