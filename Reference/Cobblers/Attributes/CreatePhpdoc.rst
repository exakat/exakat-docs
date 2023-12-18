.. _attributes-createphpdoc:

.. _create-phpdoc:

Create Phpdoc
+++++++++++++
Create PHPdoc comments for classes, interfaces, traits, methods and functions.

Parameters and return types are collected, along with the name of the structure.


.. _create-phpdoc-before:

Before
______
.. code-block:: php

   <?php
   
   class y {
       function a1(string $error, R $r = null) : int|string
       {
   
       }
   ?>

.. _create-phpdoc-after:

After
_____
.. code-block:: php

   <?php
   
   /**
    * Name : y
    */
   class y {
      /**
       * Name : a1
       *
       * string $error
       * null|R $r
       * @return int|string
       *
       */
       function a1(string $error, R $r = null) : int|string
       {
   
       }
   ?>

.. _create-phpdoc-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Attributes/RemovePhpdoc <no-anchor-for-attributes-removephpdoc>`



.. _create-phpdoc-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Attributes/CreatePhpdoc                                                                                                 |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


