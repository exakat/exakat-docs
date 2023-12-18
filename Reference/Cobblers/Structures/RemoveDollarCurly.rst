.. _structures-removedollarcurly:

.. _remove-dollar-curly:

Remove Dollar Curly
+++++++++++++++++++
This cobbler transforms the ```` structure into ``{$ }``. It is assumed that the content of the curly braces are only a variable name.

This update is important for PHP 8.2, where the syntax is deprecated.



.. _remove-dollar-curly-before:

Before
______
.. code-block:: php

   <?php
   
   $a = "";
   
   ?>

.. _remove-dollar-curly-after:

After
_____
.. code-block:: php

   <?php
   
   $a = "{$b}";
   
   ?>



.. _remove-dollar-curly-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveDollarCurly                                                                                            |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


