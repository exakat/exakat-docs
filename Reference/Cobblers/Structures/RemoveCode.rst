.. _structures-removecode:

.. meta::
	:description:
		Remove Instructions: Removes atomic instructions from the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Instructions
	:twitter:description: Remove Instructions: Removes atomic instructions from the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Instructions
	:og:type: article
	:og:description: Removes atomic instructions from the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RemoveCode.html
	:og:locale: en

.. _remove-instructions:

Remove Instructions
+++++++++++++++++++
Removes atomic instructions from the code. The whole expression is removed, and the slot is closed. 

This cobbler works with element of a block, and not with part of larger expression (like remove a condition in a if/then, or remove the block expression of a while). 

.. _remove-instructions-before:

Before
______
.. code-block:: php

   <?php
       $a = 1; // Code to be removed
       foo(1); 
       
       do          // can remove the while expression
           ++$a;   // removing the block of the do...wihle will generate an compilation error
       while ($a < 10);
       
   ?>

.. _remove-instructions-after:

After
_____
.. code-block:: php

   <?php
       foo(1); 
   ?>

.. _remove-instructions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`useless-instructions`



.. _remove-instructions-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveCode                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


