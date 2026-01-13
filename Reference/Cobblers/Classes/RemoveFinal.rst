.. _classes-removefinal:

.. _remove-final:

Remove Final
++++++++++++
This cobbler removes the ``final`` keyword on classes and methods.

.. _remove-final-before:

Before
______
.. code-block:: php

   <?php
   
   final class y {
       final function foo() {}
   }
   
   ?>
   

.. _remove-final-after:

After
_____
.. code-block:: php

   <?php
   
   class y {
       function foo() {}
   }
   
   ?>
   

.. _remove-final-related-cobbler:

Related Cobblers
________________

* :ref:`add-final-class`
* :ref:`No anchor for Classes/AddFinalMethod <no-anchor-for-classes-addfinalmethod>`

.. _remove-final-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`add-final-class`
* :ref:`No anchor for Classes/AddFinalMethod <no-anchor-for-classes-addfinalmethod>`



.. _remove-final-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveFinal                                                                                                     |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


