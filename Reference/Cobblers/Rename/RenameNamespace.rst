.. _rename-renamenamespace:

.. _rename-a-namespace:

Rename A Namespace
++++++++++++++++++
Changes the name of a namespaces from A to B.

Make sure that the new namspace is distinct from the previous ones : merging namespaces is not recommended nor checked. This cobbler is better suited a giving an unused name to a namespace.


.. _rename-a-namespace-before:

Before
______
.. code-block:: php

   <?php
   namespace A;
   
   function foo() {} 
   
   ?>
   

.. _rename-a-namespace-after:

After
_____
.. code-block:: php

   <?php
   namespace B;
   
   function foo() {} 
   ?>


.. _rename-a-namespace-destination:

Parameters
__________

+-------------+---------+--------+----------------------------+
| Name        | Default | Type   | Description                |
+-------------+---------+--------+----------------------------+
| origin      |         | string | The original namespace.    |
+-------------+---------+--------+----------------------------+
| destination |         | string | The destination namespace. |
+-------------+---------+--------+----------------------------+

.. _rename-a-namespace-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`rename-a-namespace`



.. _rename-a-namespace-specs:

Specs
_____

+----------------+------------------------+
| Short Name     | Rename/RenameNamespace |
+----------------+------------------------+
| Exakat version | 2.6.0                  |
+----------------+------------------------+
| Available in   |                        |
+----------------+------------------------+


