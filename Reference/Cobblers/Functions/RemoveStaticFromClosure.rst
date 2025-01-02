.. _functions-removestaticfromclosure:

.. meta::
	:description:
		Remove Static From Closures And Arrow Functions: Removes the static option from closures and arrow functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Static From Closures And Arrow Functions
	:twitter:description: Remove Static From Closures And Arrow Functions: Removes the static option from closures and arrow functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Static From Closures And Arrow Functions
	:og:type: article
	:og:description: Removes the static option from closures and arrow functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Functions/RemoveStaticFromClosure.html
	:og:locale: en

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


