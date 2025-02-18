.. _structures-logicaltoinarray:

.. meta::
	:description:
		Logical To in_array(): This cobbler turns lists of ``or`` calls into a in_array() call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Logical To in_array()
	:twitter:description: Logical To in_array(): This cobbler turns lists of ``or`` calls into a in_array() call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Logical To in_array()
	:og:type: article
	:og:description: This cobbler turns lists of ``or`` calls into a in_array() call
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/LogicalToInarray.html
	:og:locale: en

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

* :ref:`logical-to-in\_array()`



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


