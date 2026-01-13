.. _structures-removenoscream:

.. _remove-noscream-@:

Remove Noscream @
+++++++++++++++++
Removes the @ operator.

.. _remove-noscream-@-before:

Before
______
.. code-block:: php

   <?php
       @$a;
   ?>

.. _remove-noscream-@-after:

After
_____
.. code-block:: php

   <?php
       $a;
   ?>

.. _remove-noscream-@-suggested-analysis:

Suggested Analysis
__________________

* :ref:`@-operator`

.. _remove-noscream-@-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _remove-noscream-@-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveNoScream                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


