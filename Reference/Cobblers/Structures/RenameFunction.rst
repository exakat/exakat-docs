.. _structures-renamefunction:

.. meta::
	:description:
		Rename A Function: Give a function with a new name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rename A Function
	:twitter:description: Rename A Function: Give a function with a new name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rename A Function
	:og:type: article
	:og:description: Give a function with a new name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RenameFunction.html
	:og:locale: en

.. _rename-a-function:

Rename A Function
+++++++++++++++++
Give a function with a new name. 

This cobbler doesn't update the name of the functioncalls. 

This cobbler may be used with functions, and methods. Functions may be identified with their fully qualified name (i.e. \path\foo) and methods with the extended fully qualified name (i.e. : \path\aClass::methodName). 



.. _rename-a-function-before:

Before
______
.. code-block:: php

   <?php
       function foo() {
       
       }
   ?>

.. _rename-a-function-after:

After
_____
.. code-block:: php

   <?php
       function bar() {
       
       }
   ?>


.. _rename-a-function-name:

Parameters
__________

+------+---------+--------+-------------------------------+
| Name | Default | Type   | Description                   |
+------+---------+--------+-------------------------------+
| name | foo     | string | The new name of the function. |
+------+---------+--------+-------------------------------+

.. _rename-a-function-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _rename-a-function-related-cobbler:

Related Cobblers
________________

* :ref:`rename-functioncalls`

.. _rename-a-function-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _rename-a-function-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RenameFunction                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


