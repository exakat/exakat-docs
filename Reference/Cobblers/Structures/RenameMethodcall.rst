.. _structures-renamemethodcall:

.. _rename-methodcall:

Rename Methodcall
+++++++++++++++++
Rename a method, in a methodcall, with a new name. 

This cobbler doesn't update the definition of the method. It works both on static and non-static methods. 



.. _rename-methodcall-before:

Before
______
.. code-block:: php

   <?php
       $o->method();
   ?>

.. _rename-methodcall-after:

After
_____
.. code-block:: php

   <?php
       $o->newName();
   ?>


.. _rename-methodcall-destination:

Parameters
__________

+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| Name        | Default       | Type   | Description                                                                             |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| origin      | strtolower    | string | The function name to rename. It will be use lower-cased, and as a fully qualified name. |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| destination | mb_strtolower | string | The function name to rename. It will be use as is. FQN is possible.                     |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+

.. _rename-methodcall-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _rename-methodcall-related-cobbler:

Related Cobblers
________________

* :ref:`rename-functioncalls`
* :ref:`rename-a-function`

.. _rename-methodcall-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Structures/RemoveMethodCall <no-anchor-for-structures-removemethodcall>`



.. _rename-methodcall-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RenameMethodcall                                                                                             |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


