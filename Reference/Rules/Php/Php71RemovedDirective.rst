.. _php-php71removeddirective:


.. _php-7.1-removed-directives:

PHP 7.1 Removed Directives
++++++++++++++++++++++++++

.. meta::
	:description:
		PHP 7.1 Removed Directives: List of directives that are removed in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.1 Removed Directives
	:twitter:description: PHP 7.1 Removed Directives: List of directives that are removed in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.1 Removed Directives
	:og:type: article
	:og:description: List of directives that are removed in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.1 Removed Directives.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php71RemovedDirective.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php71RemovedDirective.html","name":"PHP 7.1 Removed Directives","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"List of directives that are removed in PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.1 Removed Directives.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of directives that are removed in PHP 7.1.

+ session.hash_function
+ session.hash_bits_per_charactor
+ session.entropy_file
+ session.entropy_length

.. code-block:: php
   
   <?php
   
   ini_get('session.hash_function');
   
   ?>

See also `Removed INI directives <https://www.php.net/manual/en/migration71.incompatible.php#migration71.incompatible.removed-ini-directives>`_.

Connex PHP features
-------------------

  + `Directives <https://php-dictionary.readthedocs.io/en/latest/dictionary/directive.ini.html>`_
  + `removed-feature <https://php-dictionary.readthedocs.io/en/latest/dictionary/removed-feature.ini.html>`_


Suggestions
___________

* Remove the code related to those directives




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php71RemovedDirective                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and more recent                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


