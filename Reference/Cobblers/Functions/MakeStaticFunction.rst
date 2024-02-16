.. _functions-makestaticfunction:

.. _make-static-closures-and-arrow-functions:

Make Static Closures And Arrow Functions
++++++++++++++++++++++++++++++++++++++++
Add the static option to closures and arrow functions. This prevents the defining environment to be included in the closure.



.. _make-static-closures-and-arrow-functions-before:

Before
______
.. code-block:: php

   <?php
       $a = function () { return 1; };
       $b = fn () => 2;
   ?>
   

.. _make-static-closures-and-arrow-functions-after:

After
_____
.. code-block:: php

   <?php
       $a = static function () { return 1; };
       $b = static fn () => 2;
   ?>

.. _make-static-closures-and-arrow-functions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-static-closure`

.. _make-static-closures-and-arrow-functions-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Functions/RemoveStaticFromFunction <no-anchor-for-functions-removestaticfromfunction>`



.. _make-static-closures-and-arrow-functions-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/MakeStaticFunction                                                                                            |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


