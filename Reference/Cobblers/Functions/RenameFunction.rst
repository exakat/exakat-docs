.. _functions-renamefunction:

.. _rename-a-function:

Rename A Function
+++++++++++++++++
This cobbler renames a function from a name A to a name B. 




.. _rename-a-function-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {} 
   foo();
   
   ?>

.. _rename-a-function-after:

After
_____
.. code-block:: php

   <?php
   
   function bar() {} 
   bar();
   
   ?>


.. _rename-a-function-destination:

Parameters
__________

+-------------+---------+--------+---------------------------------+
| Name        | Default | Type   | Description                     |
+-------------+---------+--------+---------------------------------+
| origin      |         | string | The function to rename          |
+-------------+---------+--------+---------------------------------+
| destination |         | string | The destination's function name |
+-------------+---------+--------+---------------------------------+

.. _rename-a-function-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-a-function`



.. _rename-a-function-specs:

Specs
_____

+----------------+--------------------------+
| Short Name     | Functions/RenameFunction |
+----------------+--------------------------+
| Exakat version | 2.3.0                    |
+----------------+--------------------------+
| Available in   |                          |
+----------------+--------------------------+


