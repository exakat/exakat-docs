.. _structures-removevariable:

.. _remove-written-only-variable:

Remove Written Only Variable
++++++++++++++++++++++++++++
This removes variables that are written only. 

.. _remove-written-only-variable-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {
       $a = 1;
       $a += 2; // No usage of $a
   }
   
   ?>

.. _remove-written-only-variable-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() {
   }
   
   ?>

.. _remove-written-only-variable-suggested-analysis:

Suggested Analysis
__________________

* :ref:`written-only-variables`



.. _remove-written-only-variable-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveVariable                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


