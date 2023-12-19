.. _classes-multiplepropertydeclaration:

.. _multiple-property-declaration:

Multiple Property Declaration
+++++++++++++++++++++++++++++

  The same property is declared in various classes, at least two, in the same class hierarchy. The declarations must be compatible one another, and one of them should be sufficient. 

Generally, the higher declaration should be the one to stay. 

Keeping one definition makes it clear which class is responsible for that property. It also keep the code more flexible in case of an update on the property: only one place to change it.



.. code-block:: php
   
   <?php
   
   class x {
   	// redeclared in y
   	public $p = 1;
   	
   	// declared only in x;
   	public $q;
   }
   
   class y extends x {
   	// redeclared in x
   	public $p = 2;
   
   	// declared only in y;
   	public $q;
   }
   
   ?>

Suggestions
___________

* Remove all but one of the declarations
* Change the name of some of the properties, to keep their meaning separate




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MultiplePropertyDeclaration                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | dry                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


