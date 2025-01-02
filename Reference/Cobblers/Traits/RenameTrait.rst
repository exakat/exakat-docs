.. _traits-renametrait:

.. meta::
	:description:
		Rename Trait: Rename a trait into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Trait
	:twitter:description: Rename Trait: Rename a trait into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Trait
	:og:type: article
	:og:description: Rename a trait into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Traits/RenameTrait.html
	:og:locale: en

.. _rename-trait:

Rename Trait
++++++++++++
Rename a trait into another one. 

The rename applies the new name to the trait, and its usage : use cases in classes and traits, static calls (PHP 8.0-). 

.. _rename-trait-before:

Before
______
.. code-block:: php

   <?php
   trait T {}
   
   class X {
   	use t;
   }
   
   ?>

.. _rename-trait-after:

After
_____
.. code-block:: php

   <?php
   trait newT {}
   
   class x {
   	use newT;
   }
   
   ?>


.. _rename-trait-destination:

Parameters
__________

+-------------+---------+--------+------------------------------+
| Name        | Default | Type   | Description                  |
+-------------+---------+--------+------------------------------+
| origin      |         | string | The class to rename          |
+-------------+---------+--------+------------------------------+
| destination |         | string | The destination's class name |
+-------------+---------+--------+------------------------------+



.. _rename-trait-specs:

Specs
_____

+----------------+--------------------+
| Short Name     | Traits/RenameTrait |
+----------------+--------------------+
| Exakat version | 2.3.0              |
+----------------+--------------------+
| Available in   |                    |
+----------------+--------------------+


