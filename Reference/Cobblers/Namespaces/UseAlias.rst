.. _namespaces-usealias:

.. meta::
	:description:
		Use Available Alias: Apply systematically the use expression in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Available Alias
	:twitter:description: Use Available Alias: Apply systematically the use expression in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Available Alias
	:og:type: article
	:og:description: Apply systematically the use expression in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Namespaces/UseAlias.html
	:og:locale: en

.. _use-available-alias:

Use Available Alias
+++++++++++++++++++
Apply systematically the use expression in the code.

.. _use-available-alias-before:

Before
______
.. code-block:: php

   <?php
       use A\B\C as D;
       new A\B\C();
   ?>
   

.. _use-available-alias-after:

After
_____
.. code-block:: php

   <?php
       use A\B\C as D;
       new D();
   ?>

.. _use-available-alias-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-use-alias`



.. _use-available-alias-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Namespaces/UseAlias                                                                                                     |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


