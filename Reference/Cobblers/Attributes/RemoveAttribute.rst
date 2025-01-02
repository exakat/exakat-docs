.. _attributes-removeattribute:

.. meta::
	:description:
		Remove The Attribute: Remove attributes from all supporting structures.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove The Attribute
	:twitter:description: Remove The Attribute: Remove attributes from all supporting structures
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove The Attribute
	:og:type: article
	:og:description: Remove attributes from all supporting structures
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Attributes/RemoveAttribute.html
	:og:locale: en

.. _remove-the-attribute:

Remove The Attribute
++++++++++++++++++++
Remove attributes from all supporting structures.

Attributes are located on functions, classes, class constants, properties, methods and arguments.


.. _remove-the-attribute-before:

Before
______
.. code-block:: php

   <?php
   
   #[Attribute] 
   function foo(#[AttributeArgument] $arg) {
   
   }
   ?>

.. _remove-the-attribute-after:

After
_____
.. code-block:: php

   <?php
   
   
   function foo($arg) {
   
   }
   ?>



.. _remove-the-attribute-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Attributes/RemoveAttribute                                                                                              |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


