.. _php-php70removedfunctions:

.. _php-7.0-removed-functions:

PHP 7.0 Removed Functions
+++++++++++++++++++++++++

.. meta\:\:
	:description:
		PHP 7.0 Removed Functions: The following PHP native functions were removed in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.0 Removed Functions
	:twitter:description: PHP 7.0 Removed Functions: The following PHP native functions were removed in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.0 Removed Functions
	:og:type: article
	:og:description: The following PHP native functions were removed in PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php70RemovedFunctions.html
	:og:locale: en
  The following PHP native functions were removed in PHP 7.0.

* ereg()
* ereg_replace()
* eregi()
* eregi_replace()
* split()
* spliti()
* sql_regcase()
* `magic_quotes_runtime() <https://www.php.net/magic_quotes_runtime>`_
* `set_magic_quotes_runtime() <https://www.php.net/set_magic_quotes_runtime>`_
* call_user_method()
* call_user_method_array()
* set_socket_blocking()
* mcrypt_ecb()
* mcrypt_cbc()
* mcrypt_cfb()
* mcrypt_ofb()
* datefmt_set_timezone_id()
* imagepsbbox()
* imagepsencodefont()
* imagepsextendfont()
* imagepsfreefont()
* imagepsloadfont()
* imagepsslantfont()
* imagepstext()

This analysis skips redefined PHP functions : when a replacement for a removed PHP function was created, with condition on the PHP version, then its usage is considered valid.

See also `PHP 7.0 Removed Functions <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.removed-functions>`_.


Suggestions
___________

* Replace the old functions with modern functions
* Remove the usage of the old functions
* Create an alternative function by wiring the old name to a new feature




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php70RemovedFunctions                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


