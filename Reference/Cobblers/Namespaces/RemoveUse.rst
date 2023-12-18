.. _namespaces-removeuse:

.. _remove-unused-use:

Remove Unused Use
+++++++++++++++++
Removes the unused use expression from the top of the file. Groupuse are not processed yet.

.. _remove-unused-use-before:

Before
______
.. code-block:: php

   <?php
   
   use a\b;
   use c\d;
   
   new b();
   
   ?>

.. _remove-unused-use-after:

After
_____
.. code-block:: php

   <?php
   
   use a\b;
   
   new b();
   
   ?>

.. _remove-unused-use-suggested-analysis:

Suggested Analysis
__________________

* :ref:`unused-use`



.. _remove-unused-use-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Namespaces/RemoveUse                                                                                                    |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


