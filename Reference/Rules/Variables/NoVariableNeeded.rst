.. _variables-novariableneeded:

.. _no-variable-needed:

No Variable Needed
++++++++++++++++++

.. meta::
	:description:
		No Variable Needed: This analysis reports methods where the local variables are not needed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Variable Needed
	:twitter:description: No Variable Needed: This analysis reports methods where the local variables are not needed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Variable Needed
	:og:type: article
	:og:description: This analysis reports methods where the local variables are not needed
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/NoVariableNeeded.html
	:og:locale: en
This analysis reports methods where the local variables are not needed.

Such variables may be used to improve readability. 


.. code-block:: php
   
   <?php
   
   // The variable is not strictly necessary here
   function foo($a) {
   	$k = $a->method(1, 0);
   	return $k;
   }
   
   ?>

Suggestions
___________

* Remove the variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/NoVariableNeeded                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
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


