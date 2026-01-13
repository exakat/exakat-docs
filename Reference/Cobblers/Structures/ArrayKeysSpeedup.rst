.. _structures-arraykeysspeedup:

.. _array\_key\_exists()-speedup:

array_key_exists() Speedup
++++++++++++++++++++++++++
array_key_exists() is sped up when declared with a use expression.

.. _array\_key\_exists()-speedup-before:

Before
______
.. code-block:: php

   <?php
   
   namespace A {
       array_key_exists($a, $b);
   }
   
   ?>

.. _array\_key\_exists()-speedup-after:

After
_____
.. code-block:: php

   <?php
   
   namespace A {
       use function array_key_exists;
       
       array_key_exists($a, $b);
   }
   
   ?>

.. _array\_key\_exists()-speedup-suggested-analysis:

Suggested Analysis
__________________

* :ref:`always-use-function-with-array\_key\_exists()`
* :ref:`array\_key\_exists()-speedup`



.. _array\_key\_exists()-speedup-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/ArrayKeysSpeedup                                                                                             |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


