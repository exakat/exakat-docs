.. _php-php74removedfunctions:


.. _php-7.4-removed-functions:

PHP 7.4 Removed Functions
+++++++++++++++++++++++++

.. meta::
	:description:
		PHP 7.4 Removed Functions: The following PHP native functions were deprecated in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.4 Removed Functions
	:twitter:description: PHP 7.4 Removed Functions: The following PHP native functions were deprecated in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.4 Removed Functions
	:og:type: article
	:og:description: The following PHP native functions were deprecated in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.4 Removed Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php74RemovedFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php74RemovedFunctions.html","name":"PHP 7.4 Removed Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following PHP native functions were deprecated in PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.4 Removed Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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

Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `Native <https://php-dictionary.readthedocs.io/en/latest/dictionary/native.ini.html>`_


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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


