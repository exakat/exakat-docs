.. _functions-settypevoid:

.. meta::
	:description:
		Set Type Void: Adds the void typehint to functions and methods, when possible.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Type Void
	:twitter:description: Set Type Void: Adds the void typehint to functions and methods, when possible
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Type Void
	:og:type: article
	:og:description: Adds the void typehint to functions and methods, when possible
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Functions/SetTypeVoid.html
	:og:locale: en

.. _set-type-void:

Set Type Void
+++++++++++++
Adds the void typehint to functions and methods, when possible.

.. _set-type-void-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {
       return;
   }
   
   ?>

.. _set-type-void-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() : void {
       return;
   }
   
   ?>

.. _set-type-void-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-void`

.. _set-type-void-related-cobbler:

Related Cobblers
________________

* :ref:`set-typehints`
* :ref:`set-null-type`

.. _set-type-void-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-type`



.. _set-type-void-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/SetTypeVoid                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


