.. _namespaces-removeuse:

.. meta::
	:description:
		Remove Unused Use: Removes the unused use expression from the top of the file.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Unused Use
	:twitter:description: Remove Unused Use: Removes the unused use expression from the top of the file
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Unused Use
	:og:type: article
	:og:description: Removes the unused use expression from the top of the file
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Namespaces/RemoveUse.html
	:og:locale: en

.. _remove-unused-use:

Remove Unused Use
+++++++++++++++++
Removes the unused use expression from the top of the file. Groupuse are not processed yet.

.. _remove-unused-use-before:

Before
______
.. code-block:: php

   <?php
   
   use a\b;
   use c\d;
   
   new b();
   
   ?>

.. _remove-unused-use-after:

After
_____
.. code-block:: php

   <?php
   
   use a\b;
   
   new b();
   
   ?>

.. _remove-unused-use-suggested-analysis:

Suggested Analysis
__________________

* :ref:`unused-use`



.. _remove-unused-use-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Namespaces/RemoveUse                                                                                                    |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


