.. _structures-renamefunctioncall:

.. meta::
	:description:
		Rename FunctionCalls: Rename a function call to another function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename FunctionCalls
	:twitter:description: Rename FunctionCalls: Rename a function call to another function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename FunctionCalls
	:og:type: article
	:og:description: Rename a function call to another function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RenameFunctionCall.html
	:og:locale: en

.. _rename-functioncalls:

Rename FunctionCalls
++++++++++++++++++++
Rename a function call to another function.

.. _rename-functioncalls-before:

Before
______
.. code-block:: php

   <?php
       foo(1, 2);
   ?>

.. _rename-functioncalls-after:

After
_____
.. code-block:: php

   <?php
       bar(1, 2);
   ?>


.. _rename-functioncalls-destination:

Parameters
__________

+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| Name        | Default       | Type   | Description                                                                             |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| origin      | strtolower    | string | The function name to rename. It will be use lower-cased, and as a fully qualified name. |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| destination | mb_strtolower | string | The function name to rename. It will be use as is. FQN is possible.                     |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+

.. _rename-functioncalls-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _rename-functioncalls-related-cobbler:

Related Cobblers
________________

* :ref:`rename-a-function`
* :ref:`rename-methodcall`

.. _rename-functioncalls-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _rename-functioncalls-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RenameFunctionCall                                                                                           |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


