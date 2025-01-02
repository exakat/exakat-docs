.. _classes-removefinal:

.. meta::
	:description:
		Remove Final: This cobbler removes the ``final`` keyword on classes and methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Final
	:twitter:description: Remove Final: This cobbler removes the ``final`` keyword on classes and methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Final
	:og:type: article
	:og:description: This cobbler removes the ``final`` keyword on classes and methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/RemoveFinal.html
	:og:locale: en

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


