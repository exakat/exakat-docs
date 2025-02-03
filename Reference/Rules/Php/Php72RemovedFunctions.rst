.. _php-php72removedfunctions:


.. _php-7.2-removed-functions:

PHP 7.2 Removed Functions
+++++++++++++++++++++++++


.. meta::

	:description:

		PHP 7.2 Removed Functions: The following PHP native functions were removed in PHP 7.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: PHP 7.2 Removed Functions

	:twitter:description: PHP 7.2 Removed Functions: The following PHP native functions were removed in PHP 7

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: PHP 7.2 Removed Functions

	:og:type: article

	:og:description: The following PHP native functions were removed in PHP 7

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.2 Removed Functions.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php72RemovedFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php72RemovedFunctions.html","name":"PHP 7.2 Removed Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following PHP native functions were removed in PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.2 Removed Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following PHP native functions were removed in PHP 7.2.

* png2wbmp()
* jpeg2wbmp()
* create_function()
* gmp_random()
* `each() <https://www.php.net/each>`_

This analysis skips redefined PHP functions : when a replacement for a removed PHP function was created, with condition on the PHP version, then its usage is considered valid.

See also `PHP 7.2 Removed Functions <https://www.php.net/manual/en/migration72.incompatible.php#migration72.incompatible.removed-functions>`_ and `Deprecated features in PHP 7.2.x <https://www.php.net/manual/en/migration72.deprecated.php>`_.

Related PHP errors 
-------------------

  + `The each() function is deprecated. This message will be suppressed on further calls <https://php-errors.readthedocs.io/en/latest/messages/the-each%28%29-function-is-deprecated.-this-message-will-be-suppressed-on-further-calls.html>`_




Suggestions
___________

* Replace the old functions with modern functions
* Remove the usage of the old functions
* Create an alternative function by wiring the old name to a new feature




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php72RemovedFunctions                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


