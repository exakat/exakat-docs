.. _php-php74removedfunctions:

.. _php-7.4-removed-functions:

PHP 7.4 Removed Functions
+++++++++++++++++++++++++

  The following PHP native functions were deprecated in PHP 7.4.

* `hebrevc() <https://www.php.net/hebrevc>`_
* `convert_cyr_string() <https://www.php.net/convert_cyr_string>`_
* `ezmlm_hash() <https://www.php.net/ezmlm_hash>`_
* `money_format() <https://www.php.net/money_format>`_
* `restore_include_path() <https://www.php.net/restore_include_path>`_
* `get_magic_quotes_gpc() <https://www.php.net/get_magic_quotes_gpc>`_
* `get_magic_quotes_runtime() <https://www.php.net/get_magic_quotes_runtime>`_

This analysis skips redefined PHP functions : when a replacement for a removed PHP function was created, with condition on the PHP version, then its usage is considered valid.

.. code-block:: php
   
   <?php
   
   // are the magic quotes in use? (before PHP 8.0)
   var_dump(get_magic_quotes_gpc());
   
   ?>

See also `PHP 7.4 Removed Functions <https://www.php.net/manual/en/migration74.incompatible.php#migration70.incompatible.removed-functions>`_ and `PHP 7.4 Deprecations : Introduction <https://wiki.php.net/rfc/deprecations_php_7_4#introduction>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php74RemovedFunctions                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.3 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | function, native                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


