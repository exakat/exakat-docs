.. _functions-removestaticfromclosure:

.. _remove-static-from-closures-and-arrow-functions:

Remove Static From Closures And Arrow Functions
+++++++++++++++++++++++++++++++++++++++++++++++
Removes the static option from closures and arrow functions.



.. _remove-static-from-closures-and-arrow-functions-before:

Before
______
.. code-block:: php

   <?php
       $a = static function () { return 1; };
       $b = static fn () => 2;
   ?>
   

.. _remove-static-from-closures-and-arrow-functions-after:

After
_____
.. code-block:: php

   <?php
       $a = function () { return 1; };
       $b = fn () => 2;
   ?>

.. _remove-static-from-closures-and-arrow-functions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`cannot-use-static-for-closure`

.. _remove-static-from-closures-and-arrow-functions-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`make-static-closures-and-arrow-functions`



.. _remove-static-from-closures-and-arrow-functions-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/RemoveStaticFromClosure                                                                                       |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


