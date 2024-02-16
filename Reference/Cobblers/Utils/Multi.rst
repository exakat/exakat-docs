.. _utils-multi:

.. _multiple-cobbler:

Multiple cobbler
++++++++++++++++
Allows to configure multiple cobbler in one file. The file is a YAML file, and must be located in the project's folder. 

The file containts a root object 'cobbler', filled with an array of cobblers, and their related configuration. Cobblers may be repeated as often as necessary.

cobblers:
- Functions/RenameParameter:
    oldName: $a
    newName: $b
    method: \foo
- Functions/RenameParameter:
    oldName: $a2
    newName: $b
    method: \foo2

The order of the configuration file is the order of execution. Do not rely on it.



.. _multiple-cobbler-before:

Before
______
.. code-block:: php

   

.. _multiple-cobbler-after:

After
_____
.. code-block:: php

   


.. _multiple-cobbler-configfile:

Parameters
__________

+------------+---------+--------+---------------------------------------+
| Name       | Default | Type   | Description                           |
+------------+---------+--------+---------------------------------------+
| configFile |         | string | The .yaml file in the project folder. |
+------------+---------+--------+---------------------------------------+



.. _multiple-cobbler-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Utils/Multi                                                                                                             |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


