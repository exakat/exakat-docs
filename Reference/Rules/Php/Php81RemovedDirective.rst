.. _php-php81removeddirective:

.. _php-8.1-removed-directives:

PHP 8.1 Removed Directives
++++++++++++++++++++++++++

.. meta::
	:description:
		PHP 8.1 Removed Directives: List of directives that are removed in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 8.1 Removed Directives
	:twitter:description: PHP 8.1 Removed Directives: List of directives that are removed in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 8.1 Removed Directives
	:og:type: article
	:og:description: List of directives that are removed in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 8.1 Removed Directives.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81RemovedDirective.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81RemovedDirective.html","name":"PHP 8.1 Removed Directives","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"List of directives that are removed in PHP 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 8.1 Removed Directives.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of directives that are removed in PHP 8.1.

In PHP 8.1, the following directives were removed : 

* `mysqlnd.fetch_data_copy`
* `filter.default`
* `filter.default_options`
* `auto_detect_line_endings`
* `oci8.old_oci_close_semantics`

You can detect valid directives with `ini_get() <https://www.php.net/ini_get>`_. This native function will return false, when the directive doesn't exist, while actual directive values will be returned as a string.

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Connex PHP features
-------------------

  + `directive <https://php-dictionary.readthedocs.io/en/latest/dictionary/directive.ini.html>`_


Suggestions
___________

* Remove usage of the directives.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81RemovedDirective                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`php-7.4-removed-directives`, :ref:`php-8.0-removed-directives`                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


