.. _functions-deepdefinitions:

.. _deep-definitions:

Deep Definitions
++++++++++++++++

  Structures, such as functions, classes, interfaces, traits, enum, etc. may be defined anywhere in the code, including inside functions. This is legit code for PHP. 

Since the availability of autoload, with spl_register_autoload(), there is no need for that kind of code. Structures should be defined, and accessible to the autoloading. Inclusions and deep definitions should be avoided, as they compel code to load some definitions, while autoloading will only load them if needed. 
Functions are excluded from autoload, but shall be gathered in libraries, and not hidden inside other code.

Constants definitions are tolerated inside functions : they may be used for avoiding repeat, or noting the usage of such function. 

Definitions inside a if/then statement, that include PHP version check are accepted here.

.. code-block:: php
   
   <?php
   
   class X {
       function init() {
           // myFunction is defined when and only if X::init() is called.
           if (!function_exists('myFunction'){
               function myFunction($a) {
                   return $a + 1;
               }
           })
       }
   }
   
   ?>

See also `Autoloading Classes <https://www.php.net/manual/en/language.oop5.autoload.php>`_.


Suggestions
___________

* Move function definitions to the global space : outside structures, and method.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DeepDefinitions                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-functions-deepdefinitions`                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


