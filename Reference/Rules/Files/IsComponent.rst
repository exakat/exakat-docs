.. _files-iscomponent:

.. _file-is-component:

File Is Component
+++++++++++++++++

.. meta::
	:description:
		File Is Component: Check that a file only contains definition elements, such as traits, interfaces, enumerations, declare, classes, constants, global variables, use or inclusions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: File Is Component
	:twitter:description: File Is Component: Check that a file only contains definition elements, such as traits, interfaces, enumerations, declare, classes, constants, global variables, use or inclusions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: File Is Component
	:og:type: article
	:og:description: Check that a file only contains definition elements, such as traits, interfaces, enumerations, declare, classes, constants, global variables, use or inclusions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/File Is Component.html
	:og:locale: en
Check that a file only contains definition elements, such as traits, interfaces, enumerations, declare, classes, constants, global variables, use or inclusions. 

Such a file is a component, that may be included in other code and there, used. By itself, it doesn't execute any code.

.. code-block:: php
   
   <?php
   
   declare(strict_types=1);
   
   class x {
   	// more code
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/IsComponent                                                                                                       |
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


