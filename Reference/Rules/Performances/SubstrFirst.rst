.. _performances-substrfirst:


.. _substring-first:

Substring First
+++++++++++++++

.. meta::
	:description:
		Substring First: Always start by reducing a string before applying some transformation on it.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Substring First
	:twitter:description: Substring First: Always start by reducing a string before applying some transformation on it
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Substring First
	:og:type: article
	:og:description: Always start by reducing a string before applying some transformation on it
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Substring First.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SubstrFirst.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SubstrFirst.html","name":"Substring First","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Always start by reducing a string before applying some transformation on it","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Substring First.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Always start by reducing a string before applying some transformation on it. The shorter string will be processed faster. 
The gain produced here is greater with longer strings, or greater reductions. They may also be used in loops. This is a micro-optimisation when used on short strings and single string reductions.

This works with any reduction function instead of `substr() <https://www.php.net/substr>`_, like `trim() <https://www.php.net/trim>`_, `iconv() <https://www.php.net/iconv>`_, etc.

.. code-block:: php
   
   <?php
   
   // fast version
   $result = strtolower(substr($string, $offset, $length));
   
   // slower version
   $result = substr(strtolower($string), $offset, $length);
   ?>
Connex PHP features
-------------------

  + `declare() <https://php-dictionary.readthedocs.io/en/latest/dictionary/declare.ini.html>`_


Suggestions
___________

* Always reduce the string first, then apply some transformation




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SubstrFirst                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-performances-substrfirst`, :ref:`case-prestashop-performances-substrfirst`                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


