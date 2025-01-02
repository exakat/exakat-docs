.. _traits-sidelinedmethod:

.. _sidelined-method:

Sidelined Method
++++++++++++++++

.. meta::
	:description:
		Sidelined Method: A method, defined in a trait, which is overwritten by a class's method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Sidelined Method
	:twitter:description: Sidelined Method: A method, defined in a trait, which is overwritten by a class's method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Sidelined Method
	:og:type: article
	:og:description: A method, defined in a trait, which is overwritten by a class's method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Sidelined Method.html
	:og:locale: en
A method, defined in a trait, which is overwritten by a class's method. This makes the trait's method useless and unreachable. 

It is recommended to check if this is not a typo, as the trait may not be able to work correctly.

.. code-block:: php
   
   <?php
   
   trait t {
   	function name() : string { return 'abc'; }
   	function foo() : string { return 'ddd'; }
   }
   
   class x {
   	use t;
   	
   	// This method
   	function name() : string { return 'bca'; }
   
   	//function foo is imported from the trait
   }
   
   ?>

Suggestions
___________

* Check the naming of the function in the class
* Use a 'as' expression to rename the trait's method with another name




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/SidelinedMethod                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


