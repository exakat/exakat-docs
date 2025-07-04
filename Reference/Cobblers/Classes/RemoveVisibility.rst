.. _classes-removevisibility:

.. meta::
	:description:
		Remove Visibility: Removes the visibility on constants, properties and methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Visibility
	:twitter:description: Remove Visibility: Removes the visibility on constants, properties and methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Visibility
	:og:type: article
	:og:description: Removes the visibility on constants, properties and methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RemoveVisibility.html
	:og:locale: en

.. _remove-visibility:

Remove Visibility
+++++++++++++++++
Removes the visibility on constants, properties and methods. 

For properties, the visibility is set to public. 

.. _remove-visibility-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private const x = 1;
       private $p = 2;
       private function foo() {}
       private function __construct() {}
   }
   ?>

.. _remove-visibility-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       const x = 1;
       public $p = 2;
       function foo() {}
       function __construct() {}
   }
   ?>



.. _remove-visibility-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveVisibility                                                                                                |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


