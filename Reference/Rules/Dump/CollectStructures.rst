.. _dump-collectstructures:

.. _collect-structures:

Collect Structures
++++++++++++++++++

.. meta::
	:description:
		Collect Structures: This rule collects all defined structures in the source code, with their details.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Structures
	:twitter:description: Collect Structures: This rule collects all defined structures in the source code, with their details
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Structures
	:og:type: article
	:og:description: This rule collects all defined structures in the source code, with their details
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectStructures.html
	:og:locale: en
This rule collects all defined structures in the source code, with their details.

+ Classes
+ Enums
+ Traits
+ Interfaces
+ Functions
+ Constants

.. code-block:: php
   
   <?php
   
   const X = 1;
   
   class Y {
   	private function foo() {}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectStructures                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


