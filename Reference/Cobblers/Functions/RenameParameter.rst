.. _functions-renameparameter:

.. _rename-parameter:

Rename Parameter
++++++++++++++++
Change the name of a parameter to a new name.

The destination parameter name is a constant. 
Suggestions : rename all parameters from the top method (in classes)
rename parameters $a into $b (currently, no $a available)

Limits : this cobbler doesn't check that another parameter is already using that name, nor if a local variable is also using that name. This may lead to unexpected results.


.. _rename-parameter-before:

Before
______
.. code-block:: php

   <?php
   
   foo(a: 1);
   
   function foo($a) { 
       return $a;
   }
   
   ?>

.. _rename-parameter-after:

After
_____
.. code-block:: php

   <?php
   
   foo(b: 1);
   
   function foo($b) { 
       return $b;
   }
   
   ?>


.. _rename-parameter-method:

Parameters
__________

+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| Name    | Default | Type   | Description                                                                                                      |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| oldName | $A      | string | The original name of the parameter.                                                                              |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| newName | $B      | string | The new name of the parameter.                                                                                   |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| method  |         | string | The name of the target method. Use a full qualified name for a function, and the class name::method for methods. |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+



.. _rename-parameter-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/RenameParameter                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


