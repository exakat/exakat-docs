.. _functions-makestaticfunction:

.. meta::
	:description:
		Make Static Closures And Arrow Functions: Add the static option to closures and arrow functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Make Static Closures And Arrow Functions
	:twitter:description: Make Static Closures And Arrow Functions: Add the static option to closures and arrow functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Make Static Closures And Arrow Functions
	:og:type: article
	:og:description: Add the static option to closures and arrow functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Functions/MakeStaticFunction.html
	:og:locale: en

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


