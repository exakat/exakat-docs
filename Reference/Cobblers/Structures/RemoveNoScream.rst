.. _structures-removenoscream:

.. meta::
	:description:
		Remove Noscream @: Removes the @ operator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Noscream @
	:twitter:description: Remove Noscream @: Removes the @ operator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Noscream @
	:og:type: article
	:og:description: Removes the @ operator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RemoveNoScream.html
	:og:locale: en

.. _remove-noscream-@:

Remove Noscream @
+++++++++++++++++
Removes the @ operator.

.. _remove-noscream-@-before:

Before
______
.. code-block:: php

   <?php
       @$a;
   ?>

.. _remove-noscream-@-after:

After
_____
.. code-block:: php

   <?php
       $a;
   ?>

.. _remove-noscream-@-suggested-analysis:

Suggested Analysis
__________________

* :ref:`@-operator`

.. _remove-noscream-@-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _remove-noscream-@-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveNoScream                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


