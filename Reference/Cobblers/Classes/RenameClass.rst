.. _classes-renameclass:

.. meta::
	:description:
		Rename Class: Rename a class into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Class
	:twitter:description: Rename Class: Rename a class into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Class
	:og:type: article
	:og:description: Rename a class into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RenameClass.html
	:og:locale: en

.. _rename-class:

Rename Class
++++++++++++
Rename a class into another one. 

The rename applies the new name to the class, and its usage : static calls, types, extends and instanceof. 

.. _rename-class-before:

Before
______
.. code-block:: php

   <?php
   class x {}
   
   function foo(x $a) {}
   
   ?>

.. _rename-class-after:

After
_____
.. code-block:: php

   <?php
   class Y {}
   
   function foo(Y $a) {}
   
   ?>


.. _rename-class-destination:

Parameters
__________

+-------------+---------+--------+------------------------------+
| Name        | Default | Type   | Description                  |
+-------------+---------+--------+------------------------------+
| origin      |         | string | The class to rename          |
+-------------+---------+--------+------------------------------+
| destination |         | string | The destination's class name |
+-------------+---------+--------+------------------------------+

.. _rename-class-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-class`



.. _rename-class-specs:

Specs
_____

+----------------+---------------------+
| Short Name     | Classes/RenameClass |
+----------------+---------------------+
| Exakat version | 2.3.0               |
+----------------+---------------------+
| Available in   |                     |
+----------------+---------------------+


