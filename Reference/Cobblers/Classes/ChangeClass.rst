.. _classes-changeclass:

.. _change-class:

Change Class
++++++++++++
This cobbler replaces a class by another one, and leave the original class intact.

This cobbler is useful for inserting new classes instead of native PHP or library related ones: the usage shall be changed, but not the definition. 

It might also be useful to update code, but keep older classes available for backward compatibility or fallback strategies.


.. _change-class-before:

Before
______
.. code-block:: php

   <?php
   
   class oldClass {}
   
   $a = new oldClass;
   
   ?>

.. _change-class-after:

After
_____
.. code-block:: php

   <?php
   
   class oldClass {}
   
   $a = new newClass;
   
   ?>


.. _change-class-destinationname:

Parameters
__________

+-----------------+---------+------+-------------------------------------------------------------------+
| Name            | Default | Type | Description                                                       |
+-----------------+---------+------+-------------------------------------------------------------------+
| origin          |         | name | The full namespace path name of the class to target.              |
+-----------------+---------+------+-------------------------------------------------------------------+
| newClass        |         | name | The full namespace path name of the class to use.                 |
+-----------------+---------+------+-------------------------------------------------------------------+
| destinationName |         | name | The name of the class to use. This may be used as an import alias |
+-----------------+---------+------+-------------------------------------------------------------------+

.. _change-class-related-cobbler:

Related Cobblers
________________

* :ref:`rename-class`

.. _change-class-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`change-class`



.. _change-class-specs:

Specs
_____

+----------------+---------------------+
| Short Name     | Classes/ChangeClass |
+----------------+---------------------+
| Exakat version | 2.3.0               |
+----------------+---------------------+
| Available in   |                     |
+----------------+---------------------+


