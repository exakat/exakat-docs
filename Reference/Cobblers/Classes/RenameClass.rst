.. _classes-renameclass:

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


