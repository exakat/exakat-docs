.. _php-nosubstrminusone:

.. _no-substr-minus-one:

No Substr Minus One
+++++++++++++++++++

.. meta::
	:description:
		No Substr Minus One: Negative index on string reaches offsets starting from the end of the string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Substr Minus One
	:twitter:description: No Substr Minus One: Negative index on string reaches offsets starting from the end of the string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Substr Minus One
	:og:type: article
	:og:description: Negative index on string reaches offsets starting from the end of the string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Substr Minus One.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoSubstrMinusOne.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoSubstrMinusOne.html","name":"No Substr Minus One","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Negative index on string reaches offsets starting from the end of the string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Substr Minus One.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Negative index on string reaches offsets starting from the end of the string. This is equivalent to removing the requested offset from the full length of the string.

This syntax also prevents relying on `substr() <https://www.php.net/substr>`_ to collect characters at the end of the string.

Negative index were introduced in PHP 7.1. This syntax is not compatible with PHP 7.0 and older.

.. code-block:: php
   
   <?php
   
   $string = 'abc';
   
   echo $string[1]; // a
   
   echo $string[-1]; // c
   
   //Equivalent to
   echo $string[count($string) - 1]; // c
   echo $string[2]; // c
   
   ?>

See also https://wiki.php.net/rfc/negative-string-offsets.

Connex PHP features
-------------------

  + `negative-index <https://php-dictionary.readthedocs.io/en/latest/dictionary/negative-index.ini.html>`_


Suggestions
___________

* Use the -1 index in a string, instead of a call to substr()




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoSubstrMinusOne                                                                                                                                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.5                                                                                                                                                                                                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and more recent                                                                                                                                                                                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


