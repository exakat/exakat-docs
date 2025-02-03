.. _type-hexadecimalstring:


.. _hexadecimal-in-string:

Hexadecimal In String
+++++++++++++++++++++

.. meta::
	:description:
		Hexadecimal In String: Mark strings that may be confused with hexadecimal.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Hexadecimal In String
	:twitter:description: Hexadecimal In String: Mark strings that may be confused with hexadecimal
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Hexadecimal In String
	:og:type: article
	:og:description: Mark strings that may be confused with hexadecimal
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hexadecimal In String.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/HexadecimalString.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/HexadecimalString.html","name":"Hexadecimal In String","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark strings that may be confused with hexadecimal","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hexadecimal In String.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mark strings that may be confused with hexadecimal. 

Until PHP 7.0, PHP recognizes hexadecimal numbers inside strings, and converts them accordingly. 

PHP 7.0 and until 7.1, converts the string to 0, silently. 

PHP 7.1 and later, emits a 'A non-numeric value encountered' warning, and convert the string to 0.

.. code-block:: php
   
   <?php
       $a = '0x0030';
       print $a + 1;
       // Print 49
   
       $c = '0x0030zyc';
       print $c + 1;
       // Print 49
   
       $b = 'b0x0030';
       print $b + 1;
       // Print 0
   ?>

See also `Integer Syntax <https://www.php.net/manual/en/language.types.integer.php#language.types.integer.syntax>`_.

Connex PHP features
-------------------

  + `hexadecimal <https://php-dictionary.readthedocs.io/en/latest/dictionary/hexadecimal.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/HexadecimalString                                                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`Inventory <ruleset-Inventory>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


