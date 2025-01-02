.. _classes-splitpropertydefinitions:

.. meta::
	:description:
		Split Property Definitions: Split multiple properties definition into independent definitions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Split Property Definitions
	:twitter:description: Split Property Definitions: Split multiple properties definition into independent definitions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Split Property Definitions
	:og:type: article
	:og:description: Split multiple properties definition into independent definitions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/SplitPropertyDefinitions.html
	:og:locale: en

.. _split-property-definitions:

Split Property Definitions
++++++++++++++++++++++++++
Split multiple properties definition into independent definitions. 

This applies to classes and traits. 

.. _split-property-definitions-before:

Before
______
.. code-block:: php

   <?php
       class x {
           private $x, $y, $z;
       }
   ?>
   

.. _split-property-definitions-after:

After
_____
.. code-block:: php

   <?php
       class x {
           private $x;
           private $y;
           private $z;
       }
   ?>

.. _split-property-definitions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`multiple-property-declaration-on-one-line`



.. _split-property-definitions-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/SplitPropertyDefinitions                                                                                        |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


