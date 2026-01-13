.. _classes-addfinalclass:

.. _add-final-class:

Add Final Class
+++++++++++++++
Adds ``final`` keyword to classes that can suppport it.


.. _add-final-class-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       // this class is not extended, so it might be final
   }
   
   ?>

.. _add-final-class-after:

After
_____
.. code-block:: php

   <?php
   
   final class x {
   }
   
   ?>

.. _add-final-class-suggested-analysis:

Suggested Analysis
__________________

* :ref:`class-could-be-final`

.. _add-final-class-related-cobbler:

Related Cobblers
________________

* :ref:`No anchor for Classes/AddFinalConstant <no-anchor-for-classes-addfinalconstant>`

.. _add-final-class-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-final`



.. _add-final-class-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/AddFinalClass                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


