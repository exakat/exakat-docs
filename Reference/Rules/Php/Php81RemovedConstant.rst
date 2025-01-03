.. _php-php81removedconstant:

.. _php-8.1-removed-constants:

PHP 8.1 Removed Constants
+++++++++++++++++++++++++

.. meta::
	:description:
		PHP 8.1 Removed Constants: The following PHP native constants were disabled in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 8.1 Removed Constants
	:twitter:description: PHP 8.1 Removed Constants: The following PHP native constants were disabled in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 8.1 Removed Constants
	:og:type: article
	:og:description: The following PHP native constants were disabled in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 8.1 Removed Constants.html
	:og:locale: en
The following PHP native constants were disabled in PHP 8.1. They are not removed, but they have no more effect. 

+ `MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH <https://www.php.net/MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH>`_
+ `MYSQLI_STORE_RESULT_COPY_DATA <https://www.php.net/MYSQLI_STORE_RESULT_COPY_DATA>`_
+ `FILE_BINARY <https://www.php.net/FILE_BINARY>`_
+ `FILE_TEXT <https://www.php.net/FILE_TEXT>`_
+ `FILTER_SANITIZE_STRING <https://www.php.net/FILTER_SANITIZE_STRING>`_

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Related PHP errors 
-------------------

  + `Constant %s is deprecated <https://php-errors.readthedocs.io/en/latest/messages/constant-%25s-is-deprecated.html>`_



Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Remove usage of those constants 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81RemovedConstant                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


