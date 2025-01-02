.. _classes-methodpropertyconfusion:

.. _method-property-confusion:

Method Property Confusion
+++++++++++++++++++++++++

.. meta::
	:description:
		Method Property Confusion: There might be confusion between a property and a method when they bear the same name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Property Confusion
	:twitter:description: Method Property Confusion: There might be confusion between a property and a method when they bear the same name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Property Confusion
	:og:type: article
	:og:description: There might be confusion between a property and a method when they bear the same name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Property Confusion.html
	:og:locale: en
There might be confusion between a property and a method when they bear the same name. While it is a valid PHP syntax, using the same name for properties and methods leads to possible confusion in the code.

.. code-block:: php
   
   <?php
   
   class x {
   	private $query = 1;
   	
   	function query() : void {}
   	
   	function foo() {
   		// The property is useless : it may be a call to the method, in fact
   		$this->query; 
   
   		// The method call returns nothing : PHP replaces it with NULL.
   		$c = $this->query();
   	}
   }
   
   ?>

Suggestions
___________

* Change the name : either the property, or the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodPropertyConfusion                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
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


