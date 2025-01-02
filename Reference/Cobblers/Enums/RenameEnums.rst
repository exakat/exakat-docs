.. _enums-renameenums:

.. meta::
	:description:
		Rename Enums: Rename a class into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Enums
	:twitter:description: Rename Enums: Rename a class into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Enums
	:og:type: article
	:og:description: Rename a class into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Enums/RenameEnums.html
	:og:locale: en

.. _rename-enums:

Rename Enums
++++++++++++
Rename a class into another one. 

The rename applies the new name to the class, and its usage : static calls, types, extends and instanceof. 

.. _rename-enums-before:

Before
______
.. code-block:: php

   <?php
   enum E {}
   
   function foo(E $a) {}
   
   ?>

.. _rename-enums-after:

After
_____
.. code-block:: php

   <?php
   enum EFG {}
   
   function foo(EFG $a) {}
   
   ?>


.. _rename-enums-destination:

Parameters
__________

+-------------+---------+--------+------------------------------+
| Name        | Default | Type   | Description                  |
+-------------+---------+--------+------------------------------+
| origin      |         | string | The class to rename          |
+-------------+---------+--------+------------------------------+
| destination |         | string | The destination's class name |
+-------------+---------+--------+------------------------------+

.. _rename-enums-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-enums`



.. _rename-enums-specs:

Specs
_____

+----------------+-------------------+
| Short Name     | Enums/RenameEnums |
+----------------+-------------------+
| Exakat version | 2.3.0             |
+----------------+-------------------+
| Available in   |                   |
+----------------+-------------------+


