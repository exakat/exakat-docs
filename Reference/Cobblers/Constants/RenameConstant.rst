.. _constants-renameconstant:

.. meta::
	:description:
		Rename Constant: This cobbler renames a constant and replace it with another constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Constant
	:twitter:description: Rename Constant: This cobbler renames a constant and replace it with another constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Constant
	:og:type: article
	:og:description: This cobbler renames a constant and replace it with another constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Constants/RenameConstant.html
	:og:locale: en

.. _rename-constant:

Rename Constant
+++++++++++++++
This cobbler renames a constant and replace it with another constant. 

.. _rename-constant-before:

Before
______
.. code-block:: php

   <?php
   
   const A = 1;
   
   echo A;
   echo \A;
   
   ?>

.. _rename-constant-after:

After
_____
.. code-block:: php

   <?php
   
   const B = 1;
   
   echo B;
   echo \B;
   
   ?>


.. _rename-constant-destination:

Parameters
__________

+-------------+---------+--------+---------------------------------+
| Name        | Default | Type   | Description                     |
+-------------+---------+--------+---------------------------------+
| origin      |         | string | The constant to rename          |
+-------------+---------+--------+---------------------------------+
| destination |         | string | The destination's constant name |
+-------------+---------+--------+---------------------------------+

.. _rename-constant-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-constant`



.. _rename-constant-specs:

Specs
_____

+----------------+--------------------------+
| Short Name     | Constants/RenameConstant |
+----------------+--------------------------+
| Exakat version | 2.3.0                    |
+----------------+--------------------------+
| Available in   |                          |
+----------------+--------------------------+


