.. _complete-returntypehint:

.. _add-return-typehint:

Add Return Typehint
+++++++++++++++++++

.. meta::
	:description:
		Add Return Typehint: Add returntype to methods, functions, closures and arrow functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Add Return Typehint
	:twitter:description: Add Return Typehint: Add returntype to methods, functions, closures and arrow functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Add Return Typehint
	:og:type: article
	:og:description: Add returntype to methods, functions, closures and arrow functions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/ReturnTypehint.html
	:og:locale: en
Add returntype to methods, functions, closures and arrow functions. The return types are read from the code and deduced, based on literal values, local types and operations.

.. code-block:: php
   
   <?php
   
   // This has no type, but could use int
   function foo() {
       return 1;
   }
   
   // This has no type, but could use string
   function goo(string $a) {
       return $a;
   }
   
   // This has no type, but could use string
   function hoo($a) {
       return $a - 2;
   }
   
   ?>

Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/ReturnTypehint                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`First <ruleset-First>`, :ref:`NoDoc <ruleset-NoDoc>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


