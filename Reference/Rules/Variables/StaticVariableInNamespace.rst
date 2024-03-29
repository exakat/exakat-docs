.. _variables-staticvariableinnamespace:

.. _static-variable-in-namespace:

Static Variable In Namespace
++++++++++++++++++++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables may be declared outside a function scope, but it has no usage. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are persistent between function calls, and there is not such thing as namespace call (including an 'include' call).

.. code-block:: php
   
   <?php
   
   namespace A {
   	// Static has no value here.
   	static $a = 1;
   	
   	function foo() {
   		// One useful static variable
   		static $static = 2;
   	}
   }
   
   ?>

Suggestions
___________

* Remove the 'static' keyword in the code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/StaticVariableInNamespace                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | static-variable, namespace                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


