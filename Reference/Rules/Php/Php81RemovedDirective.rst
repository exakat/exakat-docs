.. _php-php81removeddirective:

.. _php-8.1-removed-directives:

PHP 8.1 Removed Directives
++++++++++++++++++++++++++

  List of directives that are removed in PHP 8.1.

In PHP 8.1, the following directives were removed : 

* `mysqlnd.fetch_data_copy`
* `filter.default`
* `filter.default_options`
* `auto_detect_line_endings`
* `oci8.old_oci_close_semantics`

You can detect valid directives with `ini_get() <https://www.php.net/ini_get>`_. This native function will return false, when the directive doesn't exist, while actual directive values will be returned as a string.

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.


Suggestions
___________

* Remove usage of the directives.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81RemovedDirective                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


