.. _classes-renameproperty:

.. meta::
	:description:
		Rename Property: Rename a property into another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename Property
	:twitter:description: Rename Property: Rename a property into another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename Property
	:og:type: article
	:og:description: Rename a property into another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RenameProperty.html
	:og:locale: en

.. _rename-property:

Rename Property
+++++++++++++++
Rename a property into another one. 

The rename applies the new name to the property, and its usage : static calls, and normal calls.

.. _rename-property-before:

Before
______
.. code-block:: php

   <?php
   class x {
   	private $p = 1;
   	
   	function m() {
   		$this->p = 2;
   	}
   }
   
   ?>

.. _rename-property-after:

After
_____
.. code-block:: php

   <?php
   class x {
   	private $newP = 1;
   	
   	function m() {
   		$this->newP = 2;
   	}
   }
   
   ?>


.. _rename-property-destination:

Parameters
__________

+-------------+---------+--------+-------------------------------------------------------------------------------+
| Name        | Default | Type   | Description                                                                   |
+-------------+---------+--------+-------------------------------------------------------------------------------+
| origin      |         | string | The property to rename, along with its parent class. Like theClass::$property |
+-------------+---------+--------+-------------------------------------------------------------------------------+
| destination |         | string | The destination's property name. Only the name.                               |
+-------------+---------+--------+-------------------------------------------------------------------------------+



.. _rename-property-specs:

Specs
_____

+----------------+------------------------+
| Short Name     | Classes/RenameProperty |
+----------------+------------------------+
| Exakat version | 2.3.0                  |
+----------------+------------------------+
| Available in   |                        |
+----------------+------------------------+


