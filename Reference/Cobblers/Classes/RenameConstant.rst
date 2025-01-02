.. _classes-renameconstant:

.. meta::
	:description:
		Rename Class Constant: Rename a class constant into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Class Constant
	:twitter:description: Rename Class Constant: Rename a class constant into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Class Constant
	:og:type: article
	:og:description: Rename a class constant into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RenameConstant.html
	:og:locale: en

.. _rename-class-constant:

Rename Class Constant
+++++++++++++++++++++
Rename a class constant into another one. 

The rename applies the new name to the class constant, and its usage. 

.. _rename-class-constant-before:

Before
______
.. code-block:: php

   <?php
   class x {
   	const A = 1;
   }
   
   echo x::A;
   
   ?>

.. _rename-class-constant-after:

After
_____
.. code-block:: php

   <?php
   class x {
   	const B = 1;
   }
   
   echo x::B;
   
   ?>


.. _rename-class-constant-destination:

Parameters
__________

+-------------+---------+--------+----------------------------------------------------------------+
| Name        | Default | Type   | Description                                                    |
+-------------+---------+--------+----------------------------------------------------------------+
| origin      |         | string | The class constant to rename, along with its class name. \x::A |
+-------------+---------+--------+----------------------------------------------------------------+
| destination |         | string | The destination's class constant name. B                       |
+-------------+---------+--------+----------------------------------------------------------------+

.. _rename-class-constant-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-class-constant`



.. _rename-class-constant-specs:

Specs
_____

+----------------+------------------------+
| Short Name     | Classes/RenameConstant |
+----------------+------------------------+
| Exakat version | 2.3.0                  |
+----------------+------------------------+
| Available in   |                        |
+----------------+------------------------+


