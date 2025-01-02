.. _classes-removeabstract:

.. meta::
	:description:
		Remove Abstract: Remove the abstract option, from classes and methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Abstract
	:twitter:description: Remove Abstract: Remove the abstract option, from classes and methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Abstract
	:og:type: article
	:og:description: Remove the abstract option, from classes and methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RemoveAbstract.html
	:og:locale: en

.. _remove-abstract:

Remove Abstract
+++++++++++++++
Remove the abstract option, from classes and methods.


.. _remove-abstract-before:

Before
______
.. code-block:: php

   <?php
   abstract class x {
       function foo() {}
       
       abstract function moo() ;
   }
   ?>

.. _remove-abstract-after:

After
_____
.. code-block:: php

   <?php
   class x {
       function foo() {}
       
       function moo() {}
   }
   ?>



.. _remove-abstract-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveAbstract                                                                                                  |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


