.. _structures-removedollarcurly:

.. meta::
	:description:
		Remove Dollar Curly: This cobbler transforms the ```` structure into ``{$ }``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Dollar Curly
	:twitter:description: Remove Dollar Curly: This cobbler transforms the ```` structure into ``{$ }``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Dollar Curly
	:og:type: article
	:og:description: This cobbler transforms the ```` structure into ``{$ }``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RemoveDollarCurly.html
	:og:locale: en

.. _remove-dollar-curly:

Remove Dollar Curly
+++++++++++++++++++
This cobbler transforms the ```` structure into ``{$ }``. It is assumed that the content of the curly braces are only a variable name.

This update is important for PHP 8.2, where the syntax is deprecated.



.. _remove-dollar-curly-before:

Before
______
.. code-block:: php

   <?php
   
   $a = "";
   
   ?>

.. _remove-dollar-curly-after:

After
_____
.. code-block:: php

   <?php
   
   $a = "{$b}";
   
   ?>



.. _remove-dollar-curly-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveDollarCurly                                                                                            |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


