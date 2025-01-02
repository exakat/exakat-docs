.. _structures-removevariable:

.. meta::
	:description:
		Remove Written Only Variable: This removes variables that are written only.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Written Only Variable
	:twitter:description: Remove Written Only Variable: This removes variables that are written only
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Written Only Variable
	:og:type: article
	:og:description: This removes variables that are written only
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RemoveVariable.html
	:og:locale: en

.. _remove-written-only-variable:

Remove Written Only Variable
++++++++++++++++++++++++++++
This removes variables that are written only. 

.. _remove-written-only-variable-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {
       $a = 1;
       $a += 2; // No usage of $a
   }
   
   ?>

.. _remove-written-only-variable-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() {
   }
   
   ?>

.. _remove-written-only-variable-suggested-analysis:

Suggested Analysis
__________________

* :ref:`written-only-variables`



.. _remove-written-only-variable-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveVariable                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


