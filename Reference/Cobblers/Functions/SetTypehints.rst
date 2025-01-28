.. _functions-settypehints:

.. meta::
	:description:
		Set Types: Automagically add scalar types to methods and properties.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Types
	:twitter:description: Set Types: Automagically add scalar types to methods and properties
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Types
	:og:type: article
	:og:description: Automagically add scalar types to methods and properties
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Functions/SetTypehints.html
	:og:locale: en

.. _set-types:

Set Types
+++++++++
Automagically add scalar types to methods and properties. Arguments and return values are both supported. 

When multiple possible types are identified, no type is added. If a type is already set, no type is added.

Magic methods, such as __get(), __set(), __construct(), __desctruct(), etc are not modified by this cobbler. 

Methods which have parent's methods (resp. children's) are skipped for argument typing (resp return typing) : this may introduce a incompatible definition. On the other hand, methods which have children's methods (resp. parents') are modified for argument typing (resp return typing), thanks to covariance (resp. contravariance). 

Void (as a scalar type) and Null types are processed in a separate cobbler. 

By default, and in case of conflict, array is chosen over iterable and int is chosen over float. There are parameter to alter this behavior.



.. _set-types-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private int $p = 2;
   
       function foo(int $a = 1) : int {
           return intdiv($a, $this->p);
       }
   }
   ?>

.. _set-types-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       private int $p = 2;
   
       function foo(int $a = 1) : int {
           return intdiv($a, $this->p);
       }
   }
   ?>
   


.. _set-types-int\_or\_float:

Parameters
__________

+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| Name              | Default | Type   | Description                                                                                                       |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| array_or_iterable | array   | string | When array and iterable are the only suggestions, choose 'array', 'iterable', or 'omit'. By default, it is array. |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| int_or_float      | float   | string | When int and float are the only suggestions, choose 'int', 'float', or 'omit'. By default, it is float.           |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+

.. _set-types-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-void`

.. _set-types-related-cobbler:

Related Cobblers
________________

* :ref:`var-to-public`
* :ref:`split-property-definitions`
* :ref:`set-null-type`
* :ref:`set-type-void`

.. _set-types-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Functions/RemoveTypehint <no-anchor-for-functions-removetypehint>`



.. _set-types-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/SetTypehints                                                                                                  |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


