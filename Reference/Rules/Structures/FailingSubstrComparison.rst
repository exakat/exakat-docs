.. _structures-failingsubstrcomparison:

.. _failed-substr()-comparison:

Failed Substr() Comparison
++++++++++++++++++++++++++

.. meta::
	:description:
		Failed Substr() Comparison: The extracted string must be of the size of the compared string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Failed Substr() Comparison
	:twitter:description: Failed Substr() Comparison: The extracted string must be of the size of the compared string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Failed Substr() Comparison
	:og:type: article
	:og:description: The extracted string must be of the size of the compared string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Failed Substr() Comparison.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FailingSubstrComparison.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FailingSubstrComparison.html","name":"Failed Substr() Comparison","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The extracted string must be of the size of the compared string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Failed Substr() Comparison.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The extracted string must be of the size of the compared string.

This is also true for negative lengths.
This rule raise a false positive when the variable is already smaller than the expected `substr() <https://www.php.net/substr>`_ results.

This rule doesn't apply to `mb_substr() <https://www.php.net/mb_substr>`_ and `iconv_substr() <https://www.php.net/iconv_substr>`_ : those functions use the character size, not the byte size.

.. code-block:: php
   
   <?php
   
   // Possible comparison : strings and substr results are the same
   if (substr($a, 0, 3) === 'abc') { }
   if (substr($b, 4, 3) === 'abc') { }
   
   // Always failing : substr will probably provide a longer string
   if (substr($a, 0, 3) === 'ab') { }
   if (substr($a, 3, -3) === 'ab') { }
   
   // Omitted in this analysis
   if (substr($a, 0, 3) !== 'ab') { }
   
   ?>
Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Suggestions
___________

* Fix the string
* Fix the length of the string
* Put the string in a constant, and use strlen() or mb_strlen()
* Put the string in a constant, and use strlen() or mb_strlen()




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FailingSubstrComparison                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-failingsubstrcomparison`, :ref:`case-mediawiki-structures-failingsubstrcomparison`                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


