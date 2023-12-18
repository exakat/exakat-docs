.. _namespaces-gatheruse:

.. _gather-use-expression:

Gather Use Expression
+++++++++++++++++++++
Move lone use expression to the beginning of the file.

.. _gather-use-expression-before:

Before
______
.. code-block:: php

   <?php
       use A;
       ++$a;
       use B;
   ?>
   

.. _gather-use-expression-after:

After
_____
.. code-block:: php

   <?php
       use A;
       use B;
       ++$a;
   ?>

.. _gather-use-expression-suggested-analysis:

Suggested Analysis
__________________

* :ref:`hidden-use-expression`



.. _gather-use-expression-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Namespaces/GatherUse                                                                                                    |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


