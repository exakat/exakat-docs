.. _functions-settypevoid:

.. _set-type-void:

Set Type Void
+++++++++++++
Adds the void typehint to functions and methods, when possible.

.. _set-type-void-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {
       return;
   }
   
   ?>

.. _set-type-void-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() : void {
       return;
   }
   
   ?>

.. _set-type-void-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-void`

.. _set-type-void-related-cobbler:

Related Cobblers
________________

* :ref:`set-typehints`
* :ref:`set-null-type`

.. _set-type-void-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-type`



.. _set-type-void-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/SetTypeVoid                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


