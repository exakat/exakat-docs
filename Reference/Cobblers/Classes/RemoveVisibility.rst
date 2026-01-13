.. _classes-removevisibility:

.. _remove-visibility:

Remove Visibility
+++++++++++++++++
Removes the visibility on constants, properties and methods. 

For properties, the visibility is reset to public. 

.. _remove-visibility-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private const x = 1;
       private $p = 2;
       private function foo() {}
       private function __construct() {}
   }
   ?>

.. _remove-visibility-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       const x = 1;
       public $p = 2;
       function foo() {}
       function __construct() {}
   }
   ?>



.. _remove-visibility-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveVisibility                                                                                                |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


