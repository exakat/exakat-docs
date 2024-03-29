.. _classes-samenameasfile:

.. _not-same-name-as-file:

Not Same Name As File
+++++++++++++++++++++

  The class, interface or trait in this file as a different name, case included, than the file name. 

In the following example,  the file name is ``Foo.php``.

.. code-block:: php
   
   <?php
   
   // normal host of this file
   class Foo {
       // some code
   }
   
   // case-typo this file
   class foo {
       // some code
   }
   
   // strangely stored class 
   class foo {
       // some code
   }
   
   // This is valid name, but there is also a Foo class, and other classe in this file. 
   interface Foo {}
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/SameNameAsFile                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


