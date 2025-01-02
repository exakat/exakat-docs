.. _classes-renamemethod:

.. meta::
	:description:
		Rename Method: Rename a method into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Method
	:twitter:description: Rename Method: Rename a method into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Method
	:og:type: article
	:og:description: Rename a method into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RenameMethod.html
	:og:locale: en

.. _rename-method:

Rename Method
+++++++++++++
Rename a method into another one. 

The rename applies the new name to the method, and its usage : static calls, types, extends and instanceof. 

.. _rename-method-before:

Before
______
.. code-block:: php

   <?php
   class X {
   	function m() {}
   }
   
   (new X)->m();
   
   ?>

.. _rename-method-after:

After
_____
.. code-block:: php

   <?php
   class X {
   	function newM() {}
   }
   
   (new X)->newM();
   
   ?>


.. _rename-method-destination:

Parameters
__________

+-------------+---------+--------+--------------------------------------------------------------------------+
| Name        | Default | Type   | Description                                                              |
+-------------+---------+--------+--------------------------------------------------------------------------+
| origin      |         | string | The method to rename, along with its parent class. Like theClass::Method |
+-------------+---------+--------+--------------------------------------------------------------------------+
| destination |         | string | The destination's method name. Only the name.                            |
+-------------+---------+--------+--------------------------------------------------------------------------+

.. _rename-method-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-method`



.. _rename-method-specs:

Specs
_____

+----------------+----------------------+
| Short Name     | Classes/RenameMethod |
+----------------+----------------------+
| Exakat version | 2.3.0                |
+----------------+----------------------+
| Available in   |                      |
+----------------+----------------------+


