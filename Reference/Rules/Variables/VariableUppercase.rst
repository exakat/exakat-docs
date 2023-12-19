.. _variables-variableuppercase:

.. _all-uppercase-variables:

All Uppercase Variables
+++++++++++++++++++++++

  Usually, global variables are all in uppercase, so as to differentiate them easily. Though, this is not always the case, with examples like $argc, $argv or $http_response_header.

When using custom variables, try to use lowercase ``$variables``, ``$camelCase``, ``$sturdyCase`` or ``$snake_case``.


.. code-block:: php
   
   <?php
   
   // PHP super global, also identified by the initial _
   $localVariable = $_POST;
   
   // PHP globals
   $localVariable = $GLOBALS['HTTPS'];
   
   ?>

See also `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableUppercase                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | variable                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


