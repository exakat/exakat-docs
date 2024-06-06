.. _structures-conditionalstructures:

.. _conditional-structures:

Conditional Structures
++++++++++++++++++++++

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
| Features     | conditional-structure                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


