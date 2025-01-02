.. _structures-removebracketsaroundsingleinstruction:

.. meta::
	:description:
		Remove Brackets Around Single Instruction: This cobbler removes brackets when they are not compulsory.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Brackets Around Single Instruction
	:twitter:description: Remove Brackets Around Single Instruction: This cobbler removes brackets when they are not compulsory
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Brackets Around Single Instruction
	:og:type: article
	:og:description: This cobbler removes brackets when they are not compulsory
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RemoveBracketsAroundSingleInstruction.html
	:og:locale: en

.. _remove-brackets-around-single-instruction:

Remove Brackets Around Single Instruction
+++++++++++++++++++++++++++++++++++++++++
This cobbler removes brackets when they are not compulsory. This applies to single instruction, on for(), foreach(), while(), do...while() structures.

This also means that any refactoring that grows the instruction again to multiple instructions has to add the brackets again.  

There is no gain in speed or code lenght by removing those brackets.



.. _remove-brackets-around-single-instruction-before:

Before
______
.. code-block:: php

   <?php
   	foreach($i = 0; $i < 10; ++$i) { $total += 1; }
   ?>

.. _remove-brackets-around-single-instruction-after:

After
_____
.. code-block:: php

   <?php
   	foreach($i = 0; $i < 10; ++$i)  $total += 1;
   ?>

.. _remove-brackets-around-single-instruction-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`add-brackets-to-single-instructions`



.. _remove-brackets-around-single-instruction-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveBracketsAroundSingleInstruction                                                                        |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


