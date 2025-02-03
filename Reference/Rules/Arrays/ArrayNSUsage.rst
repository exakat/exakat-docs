.. _arrays-arraynsusage:

.. _short-syntax-for-arrays:

Short Syntax For Arrays
+++++++++++++++++++++++

.. meta::
	:description:
		Short Syntax For Arrays: Arrays written with the new short syntax.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Short Syntax For Arrays
	:twitter:description: Short Syntax For Arrays: Arrays written with the new short syntax
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Short Syntax For Arrays
	:og:type: article
	:og:description: Arrays written with the new short syntax
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Short Syntax For Arrays.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/ArrayNSUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/ArrayNSUsage.html","name":"Short Syntax For Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Arrays written with the new short syntax","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Short Syntax For Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Arrays written with the new short syntax. 

PHP 5.4 introduced the new short syntax, with square brackets. The previous syntax, based on the `array() <https://www.php.net/array>`_ keyword is still available.

.. code-block:: php
   
   <?php
   
   // All PHP versions array
   $a = array(1, 2, 3);
   
   // PHP 5.4+ arrays
   $a = [1, 2, 3];
   
   ?>

See also `Array <https://www.php.net/manual/en/language.types.array.php>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/ArrayNSUsage                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.3 and more recent                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


