.. _classes-renameproperty:

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


