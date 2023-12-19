.. _files-definitionsonly:

.. _definitions-only:

Definitions Only
++++++++++++++++

  File is definition only.

Definition-only files only include structure definitions : class, functions, traits, interfaces, constants, global, declare(), use and include().

Some functioncalls are also considered definition only, as they configure PHP, but don't process data : 
* `ini_set() <https://www.php.net/ini_set>`_
* error_reporting
* `register_shutdown_function() <https://www.php.net/register_shutdown_function>`_
* set_session_handler()
* `set_error_handler() <https://www.php.net/set_error_handler>`_
* `spl_autoload_register() <https://www.php.net/spl_autoload_register>`_


File A : 

.. code-block:: php
   
   <?php
   
   // This file has only definitions
   function foo() {}
   
   define('a', 1);
   
   class bar {}
   
   ?>


File B : 

.. code-block:: php
   
   <?php
   
   // This file has only definitions
   function foo() {}
   
   define('a', 1);
   
   class bar {}
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/DefinitionsOnly                                                                                                   |
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
| Features     | definition                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


