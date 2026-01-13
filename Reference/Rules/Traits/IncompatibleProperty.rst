.. _traits-incompatibleproperty:

.. _incompatible-property-between-class-and-trait:

Incompatible Property Between Class And Trait
+++++++++++++++++++++++++++++++++++++++++++++

  Reports a property definition that doesn't fit the importing class. The property definition should be identical in the trait and in the class. 

.. code-block:: php
   
   <?php
   
   trait t { 
   	private Invalid $property1; 
   
   	private Valid $property2; 
   }
   
   class xt { 
   	use t; 
   	
   	// This is incompatible with the trait
   	private OtherType $property1; 
   
   	// This is compatible with the trait
   	private Valid $property2; 
   }
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/theClass+and+theTrait+define+the+same+property+%28%24property%29+in+the+composition+of+theClass.+However%2C+the+definition+differs+and+is+considered+incompatible..html>`_




Suggestions
___________

* Make sure the property is defined identically in the class and the trait.
* Change the property definition in the class and make it distinct with the one in the trait.
* Change the property definition in the trait and make it distinct with the one in the class.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/IncompatibleProperty                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


