.. _structures-logicaltoinarray:

.. _logical-to-in\_array():

Logical To in_array()
+++++++++++++++++++++
This cobbler turns lists of ``or`` calls into a in_array() call. This is a faster and more readable expression.

.. _logical-to-in\_array()-before:

Before
______
.. code-block:: php

   <?php
   
   if ($a == 1 || $a == 2) {
   	// doSomething()
   }
   
   ?>

.. _logical-to-in\_array()-after:

After
_____
.. code-block:: php

   <?php
   
   if (in_array($a, [1, 2])) {
   	// doSomething()
   }
   
   ?>

.. _logical-to-in\_array()-suggested-analysis:

Suggested Analysis
__________________

* :ref:`logical-to-in\_array`



.. _logical-to-in\_array()-specs:

Specs
_____

+----------------+-----------------------------+
| Short Name     | Structures/LogicalToInarray |
+----------------+-----------------------------+
| Exakat version | 2.6.1                       |
+----------------+-----------------------------+
| Available in   |                             |
+----------------+-----------------------------+


