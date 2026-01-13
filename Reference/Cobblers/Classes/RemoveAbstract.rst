.. _classes-removeabstract:

.. _remove-abstract:

Remove Abstract
+++++++++++++++
Remove the abstract option, from classes and methods.


.. _remove-abstract-before:

Before
______
.. code-block:: php

   <?php
   abstract class x {
       function foo() {}
       
       abstract function moo() ;
   }
   ?>

.. _remove-abstract-after:

After
_____
.. code-block:: php

   <?php
   class x {
       function foo() {}
       
       function moo() {}
   }
   ?>



.. _remove-abstract-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/RemoveAbstract                                                                                                  |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


