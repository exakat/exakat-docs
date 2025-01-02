.. _structures-conditionalstructures:

.. _conditional-structures:

Conditional Structures
++++++++++++++++++++++

.. meta::
	:description:
		Conditional Structures: Structures that are defined, but only executed conditionally.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Conditional Structures
	:twitter:description: Conditional Structures: Structures that are defined, but only executed conditionally
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Conditional Structures
	:og:type: article
	:og:description: Structures that are defined, but only executed conditionally
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Conditional Structures.html
	:og:locale: en
Structures that are defined, but only executed conditionally.

It is possible to create conditioned functions, classes, interfaces, traits and enumerations. Constants have to be defined with `define() <https://www.php.net/define>`_ and can't use the `const` keyword.

Classes elements, such as methods, can't be conditional.

.. code-block:: php
   
   <?php
   
   if (!function_exists('array_column')) {
       function array_column($a) {
           // some PHP
       }
   }
   
   if (!class_exists('foo')) {
       class foo {
       
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `conditional-structure <https://php-dictionary.readthedocs.io/en/latest/dictionary/conditional-structure.ini.html>`_


Suggestions
___________

* Use different names, and apply autoloader.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConditionalStructures                                                                                        |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


