.. _php-php83newfunctions:

.. _new-functions-in-php-8.3:

New Functions In PHP 8.3
++++++++++++++++++++++++

  New functions are added to new PHP version.

The following functions are now native functions in PHP 8.3. It is compulsory to rename any custom function that was created in older versions. One alternative is to move the function to a custom namespace, and update the use list at the beginning of the script. 

* `json_validate() <https://www.php.net/json_validate>`_
* `mysqli_execute_query() <https://www.php.net/mysqli_execute_query>`_
* `posix_sysconf() <https://www.php.net/posix_sysconf>`_
* `posix_pathconf() <https://www.php.net/posix_pathconf>`_
* `posix_fpathconf() <https://www.php.net/posix_fpathconf>`_
* `socket_atmark() <https://www.php.net/socket_atmark>`_

Suggestions
___________

* Move custom functions with the same name to a new namespace
* Change the name of any custom functions with the same name
* Add a condition to the functions definition to avoid conflict




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php83NewFunctions                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP83 <ruleset-CompatibilityPHP83>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.3 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features     | function, native                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


