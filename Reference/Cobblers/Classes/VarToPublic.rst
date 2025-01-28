.. _classes-vartopublic:

.. meta::
	:description:
		Var To Public: Replace the var syntax with public keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Var To Public
	:twitter:description: Var To Public: Replace the var syntax with public keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Var To Public
	:og:type: article
	:og:description: Replace the var syntax with public keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Classes/VarToPublic.html
	:og:locale: en

.. _var-to-public:

Var To Public
+++++++++++++
Replace the var syntax with public keyword. 

It is also possible to replace it with protected or private, with the parameter. 

.. _var-to-public-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       var $y = 1;
   }
   ?>

.. _var-to-public-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       public $y = 1;
   }
   ?>


.. _var-to-public-var\_to\_visibility:

Parameters
__________

+-------------------+---------+--------+--------------------------------------------------------------------------------------+
| Name              | Default | Type   | Description                                                                          |
+-------------------+---------+--------+--------------------------------------------------------------------------------------+
| var_to_visibility | public  | string | The destination visibility to be used. May be one of: public, protected or private.  |
+-------------------+---------+--------+--------------------------------------------------------------------------------------+

.. _var-to-public-related-cobbler:

Related Cobblers
________________

* :ref:`set-types`



.. _var-to-public-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Classes/VarToPublic                                                                                                     |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


