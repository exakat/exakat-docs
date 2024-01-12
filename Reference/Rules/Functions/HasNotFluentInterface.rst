.. _functions-hasnotfluentinterface:

.. _method-is-not-for-fluent-interface:

Method Is Not For Fluent Interface
++++++++++++++++++++++++++++++++++

  Mark a method when it contains at least one return that doesn't return `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_. Such method cannot be used for fluent interface, which always require the current object to be returned. 

Null is not accepted here: it would `break <https://www.php.net/manual/en/control-structures.break.php>`_ the execution of the method call chains if it was returned. 


.. code-block:: php
   
   <?php
   
   class x {
   	// fluent interface : $this is chainable
   	function foo() {
   		return $this;
   	}
   
   	// Not for fluent interface : the method may return something else
   	function goo($a) {
   		if ($a == true) {
   			return $this;
   		} else {
   			return 3;
   		}
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/HasNotFluentInterface                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method, fluent-interface                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


