.. _classes-propertyinvasion:

.. _property-invasion:

Property Invasion
+++++++++++++++++

  Property invasion exports a reference from an object, for external and direct modifications. 

With a method that returns a reference, a link is created between an external variable and the private property. That way, it is possible to modify the object, without calling a property, or a method.

.. code-block:: php
   
   <?php
   
   class x {
   	private $p = 1;
   	
   	function &get() {
   		return $this->p;
   	}
   }
   
   $x = new x;
   $y = &$x->get();
   $y = 2;
   
   print $x->get(); // 2
   
   ?>
Connex PHP features
-------------------

  + `object-invasion <https://php-dictionary.readthedocs.io/en/latest/dictionary/object-invasion.ini.html>`_


Suggestions
___________

* `Invading private properties and methods in PHP <https://freek.dev/2192-invading-private-properties-and-methods-in-php>`_




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyInvasion                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


