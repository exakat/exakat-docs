.. _functions-multipledeclarations:

.. _multiple-functions-declarations:

Multiple Functions Declarations
+++++++++++++++++++++++++++++++

  Some functions are declared multiple times in the code. 

PHP accepts multiple definitions for the same functions, as long as they are not in the same file (linting `error) <https://www.php.net/error>`_, or not included simultaneously during the execution. 

This creates to several situations in which the same functions are defined multiple times : the function may be compatible with various PHP version, but their implementation may not. Or the function is part of a larger library, and sometimes only need without the rest of the library. 

It is recommended to avoid having several functions with the same name in one repository. Turn those functions into methods and load them when needed. 


.. code-block:: php
   
   <?php
   
   namespace a {
       function foo() {}
   }
   
   // Other file
   namespace a {
       function foo() {}
       function bar() {}
   }
   
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MultipleDeclarations                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.0                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | declaration                                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


