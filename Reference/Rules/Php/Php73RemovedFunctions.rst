.. _php-php73removedfunctions:

.. _php-7.3-removed-functions:

PHP 7.3 Removed Functions
+++++++++++++++++++++++++

.. meta::
	:description:
		PHP 7.3 Removed Functions: The following PHP native functions were removed in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.3 Removed Functions
	:twitter:description: PHP 7.3 Removed Functions: The following PHP native functions were removed in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.3 Removed Functions
	:og:type: article
	:og:description: The following PHP native functions were removed in PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php73RemovedFunctions.html
	:og:locale: en
The following PHP native functions were removed in PHP 7.3.

* image2wbmp()

This analysis skips redefined PHP functions : when a replacement for a removed PHP function was created, with condition on the PHP version, then its usage is considered valid.

See also `PHP 7.3 Removed Functions <https://www.php.net/manual/en/migration73.incompatible.php#migration73.incompatible.removed-functions>`_.


Suggestions
___________

* Replace the old functions with modern functions
* Remove the usage of the old functions
* Create an alternative function by wiring the old name to a new feature




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php73RemovedFunctions                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.3 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


