.. _classes-uselessmethod:

.. _useless-method:

Useless Method
++++++++++++++

.. meta::
	:description:
		Useless Method: This method is useless, as it actually does what PHP would do by default.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Method
	:twitter:description: Useless Method: This method is useless, as it actually does what PHP would do by default
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Method
	:og:type: article
	:og:description: This method is useless, as it actually does what PHP would do by default
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Method.html
	:og:locale: en
This method is useless, as it actually does what PHP would do by default. 

For example, relaying a method call to its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ is useless. Removing the method altogether has the same feature, although this doesn't apply to constructors. 

.. code-block:: php
   
   <?php
   
   class y {
   	function foo() {
   		// doSomething('foo')
   	}
   	function goo() {
   		// doSomething('goo')
   	}
   }
   
   class x extends y {
   	// No definition for goo(), so it fallback to the parent
   	
   	// This definition of foo() falls back to the parent's, 
   	// just like if it wasn't there.
   	function foo() {
   		return parent::foo();
   	}
   }
   ?>

Suggestions
___________

* Remove the useless method
* Add more code to the method body




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessMethod                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


