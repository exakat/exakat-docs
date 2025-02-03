.. _php-usematch:


.. _uses-php-8-match():

Uses PHP 8 Match()
++++++++++++++++++


.. meta::

	:description:

		Uses PHP 8 Match(): This rule reports usage of the the match() syntax.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Uses PHP 8 Match()

	:twitter:description: Uses PHP 8 Match(): This rule reports usage of the the match() syntax

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Uses PHP 8 Match()

	:og:type: article

	:og:description: This rule reports usage of the the match() syntax

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Uses PHP 8 Match().html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseMatch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseMatch.html","name":"Uses PHP 8 Match()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"This rule reports usage of the the match() syntax","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Uses PHP 8 Match().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports usage of the the `match() <https://www.php.net/manual/en/control-structures.match.php>`_ syntax.

`match() <https://www.php.net/manual/en/control-structures.match.php>`_ was introduced in PHP 8.0, and is an alternative to `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_. It is also not backward compatible with previous versions of PHP.


.. code-block:: php
   
   <?php
   
   $A = match($a) {
       'a' => 'A',
       'b' => 'B',
       default => 'd',
   };
   
   ?>

See also `match <https://www.php.net/manual/en/control-structures.match.php>`_ and `Match expression <https://php.watch/versions/8.0/match-expression>`_.

Connex PHP features
-------------------

  + `match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseMatch                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`reserved-match-keyword`                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


