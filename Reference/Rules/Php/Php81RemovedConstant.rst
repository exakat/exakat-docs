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

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81RemovedConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81RemovedConstant.html","name":"PHP 8.1 Removed Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following PHP native constants were disabled in PHP 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 8.1 Removed Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following PHP native constants were disabled in PHP 8.1. They are not removed, but they have no more effect. 

+ `MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH <https://www.php.net/mysqli_stmt_attr_update_max_length>`_
+ `MYSQLI_STORE_RESULT_COPY_DATA <https://www.php.net/mysqli_store_result_copy_data>`_
+ `FILE_BINARY <https://www.php.net/file_binary>`_
+ `FILE_TEXT <https://www.php.net/file_text>`_
+ `FILTER_SANITIZE_STRING <https://www.php.net/filter_sanitize_string>`_

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Related PHP errors 
-------------------

  + `Constant %s is deprecated <https://php-errors.readthedocs.io/en/latest/messages/constant-%25s-is-deprecated.html>`_



Connex PHP features
-------------------

  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


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


