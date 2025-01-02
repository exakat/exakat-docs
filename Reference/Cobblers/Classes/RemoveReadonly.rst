.. _classes-removereadonly:

.. meta::
	:description:
		Remove Readonly Option: Readonly is a property and class option.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Readonly Option
	:twitter:description: Remove Readonly Option: Readonly is a property and class option
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Readonly Option
	:og:type: article
	:og:description: Readonly is a property and class option
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RemoveReadonly.html
	:og:locale: en

.. _remove-readonly-option:

Remove Readonly Option
++++++++++++++++++++++
Readonly is a property and class option. This cobbler removes it from both. 

The readonly keyword is removed from property and class definitions, and from promoted properties.


.. _remove-readonly-option-before:

Before
______
.. code-block:: php

   <?php
   
   readonly class x {
       private readonly string $x;
   }
   
   ?>

.. _remove-readonly-option-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       private string $x;
   }
   
   ?>

.. _remove-readonly-option-suggested-analysis:

Suggested Analysis
__________________

* :ref:`readonly-usage`
* :ref:`class-could-be-readonly`



.. _remove-readonly-option-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveReadonly                                                                                                  |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


