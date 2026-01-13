.. _attributes-removeattribute:

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


