.. _classes-removemethod:

.. _remove-a-method-in-a-class:

Remove A Method In A Class
++++++++++++++++++++++++++
This removes a method in a class. The method name is provided with its fully qualified name : Name of the class:: name of the method. 

The method's name is a string.


.. _remove-a-method-in-a-class-before:

Before
______
.. code-block:: php

   <?php
   
   // removing method \x::method1 
   class x {
       function method1() {}
       function method2() {}
   }
   
   ?>

.. _remove-a-method-in-a-class-after:

After
_____
.. code-block:: php

   <?php
   
   // removed method \x::method1 
   class x {
       function method2() {}
   }
   
   ?>


.. _remove-a-method-in-a-class-name:

Parameters
__________

+------+------------+--------+-----------------------------------------------------------------+
| Name | Default    | Type   | Description                                                     |
+------+------------+--------+-----------------------------------------------------------------+
| name | x::method1 | string | Fully qualified name of the method to remove. Only one allowed. |
+------+------------+--------+-----------------------------------------------------------------+



.. _remove-a-method-in-a-class-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveMethod                                                                                                    |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


