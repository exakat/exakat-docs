.. _functions-removetypes:

.. _remove-type:

Remove Type
+++++++++++
This cobbler remove the type mentions in the code. This might yield some speed when executing, since those tests will be not conveyed at runtime. 

Types from arguments, method returns and properties are all removed. 


.. _remove-type-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private string $p;
       
       function foo(D\E $arg) : void {
       
       }
   }
   
   ?>

.. _remove-type-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       private $p;
       
       function foo($arg) {
       
       }
   }
   
   ?>


.. _remove-type-type\_to\_remove:

Parameters
__________

+----------------+---------+------+----------------------------------------------------------------------------------------------------------+
| Name           | Default | Type | Description                                                                                              |
+----------------+---------+------+----------------------------------------------------------------------------------------------------------+
| type_to_remove | all     | data | A comma separated list of types to remove. For example : never,string,A\B\C;. Use 'All' for everyt type. |
+----------------+---------+------+----------------------------------------------------------------------------------------------------------+

.. _remove-type-suggested-analysis:

Suggested Analysis
__________________

* :ref:`php-8.1-typehints`

.. _remove-type-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`set-typehints`



.. _remove-type-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/RemoveTypes                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.2.5                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


