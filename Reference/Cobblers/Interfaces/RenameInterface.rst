.. _interfaces-renameinterface:

.. meta::
	:description:
		Rename Interface: Rename an interface into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Interface
	:twitter:description: Rename Interface: Rename an interface into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Interface
	:og:type: article
	:og:description: Rename an interface into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Interfaces/RenameInterface.html
	:og:locale: en

.. _rename-interface:

Rename Interface
++++++++++++++++
Rename an interface into another one. 

The rename applies the new name to the class, and its usage : static constants, types, extends and instanceof. 

.. _rename-interface-before:

Before
______
.. code-block:: php

   <?php
   interface i {}
   
   function foo(i $a) : j {}
   
   ?>

.. _rename-interface-after:

After
_____
.. code-block:: php

   <?php
   class j {}
   
   function foo(j $a) : j {}
   
   ?>


.. _rename-interface-destination:

Parameters
__________

+-------------+---------+--------+------------------------------+
| Name        | Default | Type   | Description                  |
+-------------+---------+--------+------------------------------+
| origin      |         | string | The class to rename          |
+-------------+---------+--------+------------------------------+
| destination |         | string | The destination's class name |
+-------------+---------+--------+------------------------------+

.. _rename-interface-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-interface`



.. _rename-interface-specs:

Specs
_____

+----------------+----------------------------+
| Short Name     | Interfaces/RenameInterface |
+----------------+----------------------------+
| Exakat version | 2.5.0                      |
+----------------+----------------------------+
| Available in   |                            |
+----------------+----------------------------+


