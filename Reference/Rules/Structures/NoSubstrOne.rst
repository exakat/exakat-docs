.. _structures-nosubstrone:

.. _avoid-substr()-one:

Avoid Substr() One
++++++++++++++++++

.. meta::
	:description:
		Avoid Substr() One: Use array notation ``$string[$position]`` to reach a single byte in a string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Substr() One
	:twitter:description: Avoid Substr() One: Use array notation ``$string[$position]`` to reach a single byte in a string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Substr() One
	:og:type: article
	:og:description: Use array notation ``$string[$position]`` to reach a single byte in a string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid Substr() One.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoSubstrOne.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoSubstrOne.html","name":"Avoid Substr() One","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use array notation ``$string[$position]`` to reach a single byte in a string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid Substr() One.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Use array notation ``$string[$position]`` to reach a single byte in a string.

There are two ways to access a byte in a string : `substr() <https://www.php.net/substr>`_ and ``$v[$pos]``.

The second style is more readable. It may be up to four times faster, though it is a micro-optimization. It is recommended to use it. 

PHP 7.1 also introduces the support of negative offsets as string index : negative offset are also reported.
Beware that `substr() <https://www.php.net/substr>`_ and ``$v[$pos]`` are similar, while `mb_substr() <https://www.php.net/mb_substr>`_ is not. The first function works on bytes, while the latter works on characters.

.. code-block:: php
   
   <?php
   
   $string = 'ab人cde';
   
   echo substr($string, $pos, 1);
   echo $string[$pos];
   
   echo mb_substr($string, $pos, 1);
   
   // when $pos = 1
   // displays bbb
   // when $pos = 2
   // displays ??人
   
   ?>

Suggestions
___________

* Replace substr() with the array notations for strings.
* Replace substr() with a call to mb_substr().




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoSubstrOne                                                                                                                                                                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-structures-nosubstrone`, :ref:`case-livezilla-structures-nosubstrone`                                                                                                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


