.. _enums-renameenums:

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


