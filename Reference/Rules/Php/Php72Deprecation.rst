.. _php-php72deprecation:


.. _php-7.2-deprecations:

PHP 7.2 Deprecations
++++++++++++++++++++

.. meta::
	:description:
		PHP 7.2 Deprecations: Several functions are deprecated in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.2 Deprecations
	:twitter:description: PHP 7.2 Deprecations: Several functions are deprecated in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.2 Deprecations
	:og:type: article
	:og:description: Several functions are deprecated in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.2 Deprecations.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php72Deprecation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php72Deprecation.html","name":"PHP 7.2 Deprecations","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Several functions are deprecated in PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.2 Deprecations.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Several functions are deprecated in PHP 7.2. 

* `parse_str() <https://www.php.net/parse_str>`_ with no second argument
* `assert() <https://www.php.net/assert>`_ on strings
* Usage of gmp_random(), create_function(), `each() <https://www.php.net/each>`_
* Usage of (unset)
* Usage of ``$php_errormsg``
* directive ``mbstring.func_overload`` (not supported yet)

Deprecated functions and extensions are reported in a separate analysis.

See also `Deprecations for PHP 7.2 <https://wiki.php.net/rfc/deprecations_php_7_2>`_.

Connex PHP features
-------------------

  + `feature <https://php-dictionary.readthedocs.io/en/latest/dictionary/feature.ini.html>`_


Suggestions
___________

* Remove the deprecated functions, and replace them with a new feature 
* Use a replacement function to emulate this old behavior




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php72Deprecation                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.9                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


