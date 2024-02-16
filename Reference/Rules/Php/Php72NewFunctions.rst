.. _php-php72newfunctions:

.. _new-functions-in-php-7.2:

New Functions In PHP 7.2
++++++++++++++++++++++++

  The following functions are now native functions in PHP 7.2. It is advised to change custom functions that are currently created, and using those names, before moving to this new version.

* `mb_ord() <https://www.php.net/mb_ord>`_
* `mb_chr() <https://www.php.net/mb_chr>`_
* `mb_scrub() <https://www.php.net/mb_scrub>`_
* `stream_isatty() <https://www.php.net/stream_isatty>`_
* `proc_nice() <https://www.php.net/proc_nice>`_ (Windows only)

Suggestions
___________

* Move custom functions with the same name to a new namespace
* Change the name of any custom functions with the same name
* Add a condition to the functions definition to avoid conflict




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php72NewFunctions                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.7                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | function, native                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


