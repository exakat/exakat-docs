.. _functions-setnulltype:

.. meta::
	:description:
		Set Null Type: Adds a Null type to typehints when necessary.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Null Type
	:twitter:description: Set Null Type: Adds a Null type to typehints when necessary
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Null Type
	:og:type: article
	:og:description: Adds a Null type to typehints when necessary
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Functions/SetNullType.html
	:og:locale: en

.. _set-null-type:

Set Null Type
+++++++++++++
Adds a Null type to typehints when necessary. 

This cobbler only adds a null type when there is already another type. It doesn't add a null type when no type is set. 

It works on methods, functions, closures and arrow functions. It doesn't work on properties.

The null type is added as a question mark `?` when the type is unique, and as null when the types are multiple.


.. _set-null-type-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() : int {
       if (rand(0, 1)) {
           return 1;
       } else {
           return null;
       }
   }
   
   ?>

.. _set-null-type-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() : ?int {
       if (rand(0, 1)) {
           return 1;
       } else {
           return null;
       }
   }
   
   ?>

.. _set-null-type-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-type`



.. _set-null-type-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/SetNullType                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


