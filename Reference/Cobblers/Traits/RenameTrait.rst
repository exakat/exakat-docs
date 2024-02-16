.. _traits-renametrait:

.. _rename-class:

Rename Class
++++++++++++
Rename a trait into another one. 

The rename applies the new name to the trait, and its usage : use cases in classes and traits, static calls (PHP 8.0-). 

.. _rename-class-before:

Before
______
.. code-block:: php

   <?php
   trait t {}
   
   class x {
   	use t;
   }
   
   ?>

.. _rename-class-after:

After
_____
.. code-block:: php

   <?php
   trait newT {}
   
   class x {
   	use newT;
   }
   
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



.. _rename-class-specs:

Specs
_____

+----------------+--------------------+
| Short Name     | Traits/RenameTrait |
+----------------+--------------------+
| Exakat version | 2.3.0              |
+----------------+--------------------+
| Available in   |                    |
+----------------+--------------------+


