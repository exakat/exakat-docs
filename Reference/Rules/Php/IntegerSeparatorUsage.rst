.. _php-integerseparatorusage:

.. _numeric-literal-separator:

Numeric Literal Separator
+++++++++++++++++++++++++

.. meta::
	:description:
		Numeric Literal Separator: Integer and floats may be written with internal underscores.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Numeric Literal Separator
	:twitter:description: Numeric Literal Separator: Integer and floats may be written with internal underscores
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Numeric Literal Separator
	:og:type: article
	:og:description: Integer and floats may be written with internal underscores
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Numeric Literal Separator.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IntegerSeparatorUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IntegerSeparatorUsage.html","name":"Numeric Literal Separator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Integer and floats may be written with internal underscores","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Numeric Literal Separator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Integer and floats may be written with internal underscores. This way, it is possible to separate large number into smaller groups, and make them more readable.

Numeric Literal Separators were introduced in PHP 7.4 and are not backward compatible.

.. code-block:: php
   
   <?php
   $a = 1_000_000_000;   // A billion
   $a = 1000000000;      // A billion too...
   
   $b = 107_925_284.88;‬ // 6 light minute to kilometers = 107925284.88 kilometers
   $b = 107925284.88;‬   // Same as above
   ?>

See also `PHP RFC: Numeric Literal Separator <https://wiki.php.net/rfc/numeric_literal_separator>`_.

Connex PHP features
-------------------

  + `integer-separator <https://php-dictionary.readthedocs.io/en/latest/dictionary/integer-separator.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IntegerSeparatorUsage                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


