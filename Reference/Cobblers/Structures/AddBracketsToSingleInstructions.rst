.. _structures-addbracketstosingleinstructions:

.. meta::
	:description:
		Add Brackets To Single Instructions: This cobbler adds curly brackets to single expression, with for(), foreach(), while().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Add Brackets To Single Instructions
	:twitter:description: Add Brackets To Single Instructions: This cobbler adds curly brackets to single expression, with for(), foreach(), while()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Add Brackets To Single Instructions
	:og:type: article
	:og:description: This cobbler adds curly brackets to single expression, with for(), foreach(), while()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/AddBracketsToSingleInstructions.html
	:og:locale: en

.. _add-brackets-to-single-instructions:

Add Brackets To Single Instructions
+++++++++++++++++++++++++++++++++++
This cobbler adds curly brackets to single expression, with for(), foreach(), while(); and do...while() instructions. 

No brackets are added to instructions that are already bracketed.

.. _add-brackets-to-single-instructions-before:

Before
______
.. code-block:: php

   <?php
   
   if ($a) 
   	$b = 1;
   else {
   	$c = ;2
   }
   
   ?>

.. _add-brackets-to-single-instructions-after:

After
_____
.. code-block:: php

   <?php
   
   if ($a) {
   	$b = 1;
   } else {
   	$c = ;2
   }
   
   ?>

.. _add-brackets-to-single-instructions-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Structures/RemoveBracketsAroundSingleInstruction.ini <no-anchor-for-structures-removebracketsaroundsingleinstruction.ini>`



.. _add-brackets-to-single-instructions-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/AddBracketsToSingleInstructions                                                                              |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.4.6                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


