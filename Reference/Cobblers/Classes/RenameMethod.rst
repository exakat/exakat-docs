.. _classes-renamemethod:

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
   class x {
   	function m() {}
   }
   
   (new x)->m();
   
   ?>

.. _rename-class-after:

After
_____
.. code-block:: php

   <?php
   class x {
   	function newM() {}
   }
   
   (new x)->newM();
   
   ?>


.. _rename-class-destination:

Parameters
__________

+-------------+---------+--------+--------------------------------------------------------------------------+
| Name        | Default | Type   | Description                                                              |
+-------------+---------+--------+--------------------------------------------------------------------------+
| origin      |         | string | The method to rename, along with its parent class. Like theClass::Method |
+-------------+---------+--------+--------------------------------------------------------------------------+
| destination |         | string | The destination's method name. Only the name.                            |
+-------------+---------+--------+--------------------------------------------------------------------------+

.. _rename-class-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-class`



.. _rename-class-specs:

Specs
_____

+----------------+----------------------+
| Short Name     | Classes/RenameMethod |
+----------------+----------------------+
| Exakat version | 2.3.0                |
+----------------+----------------------+
| Available in   |                      |
+----------------+----------------------+


