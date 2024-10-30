.. _functions-undefinedfunctions:

.. _undefined-functions:

Undefined Functions
+++++++++++++++++++

  Those functions are called, though they are not defined in the code. 

The functions are probably defined in a missing library, component, or in an extension. When this is not the case, PHP yield a Fatal `error <https://www.php.net/error>`_ at execution.

.. code-block:: php
   
   <?php
   
   // Undefined function 
   foo($a);
   
   // valid function, as it belongs to the ext/yaml extension
   $parsed = yaml_parse($yaml);
   
   // This function is not defined in the a\b\c namespace, nor in the global namespace
   a\b\c\foo(); 
   
   ?>

See also `Functions <https://www.php.net/manual/en/language.functions.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Undefined+function.html>`_



Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_


Suggestions
___________

* Fix the name of the function in the code
* Remove the functioncall in the code
* Define the function for the code to call it
* Include the correct library in the code source




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UndefinedFunctions                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


