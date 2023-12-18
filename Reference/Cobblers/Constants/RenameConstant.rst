.. _constants-renameconstant:

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


