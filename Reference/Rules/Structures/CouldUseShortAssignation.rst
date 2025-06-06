.. _structures-coulduseshortassignation:


.. _could-use-short-assignation:

Could Use Short Assignation
+++++++++++++++++++++++++++

.. meta::
	:description:
		Could Use Short Assignation: Use short assignment operator, to speed up code, and keep syntax clear.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Short Assignation
	:twitter:description: Could Use Short Assignation: Use short assignment operator, to speed up code, and keep syntax clear
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Short Assignation
	:og:type: article
	:og:description: Use short assignment operator, to speed up code, and keep syntax clear
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Short Assignation.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseShortAssignation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseShortAssignation.html","name":"Could Use Short Assignation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use short assignment operator, to speed up code, and keep syntax clear","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Short Assignation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use short assignment operator, to speed up code, and keep syntax clear.

Some operators, like * or +, have a compact and fast 'do-and-assign' version. They looks like a compacted version for = and the operator. This syntax is good for readability, and saves some memory in the process. 

Depending on the operator, not all permutations of arguments are possible. For example, ``$a = $a - 2`` can use the ``-=`` short operator, but ``$a = 2 - $a`` doesn't. 

Addition and short assignation of addition have a different set of features when applied to arrays. Do not exchange one another in that case.

Short operators are faster than the extended version, though it is a micro-optimization.

.. code-block:: php
   
   <?php
   
   $a = 10 + $a;
   $a += 10;
   
   $b = $b - 1;
   $b -= 1;
   
   $c = $c * 2;
   $c *= 2;
   
   $d = $d / 3;
   $d /= 3;
   
   $e = $e % 4;
   $e %= 4;
   
   $f = $f | 5;
   $f |= 5;
   
   $g = $g & 6;
   $g &= 6;
   
   $h = $h ^ 7;
   $h ^= 7;
   
   $i = $i >> 8;
   $i >>= 8;
   
   $j = $j << 9;
   $j <<= 9;
   
   // PHP 7.4 and more recent
   $l = $l ?? 'value';
   $l ??= 'value';
   
   ?>

See also `Assignation Operators <https://www.php.net/manual/en/language.operators.assignment.php>`_.

Connex PHP features
-------------------

  + `Short Assignations <https://php-dictionary.readthedocs.io/en/latest/dictionary/short-assignation.ini.html>`_


Suggestions
___________

* Change the expression to use the short assignation




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseShortAssignation                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Rector <ruleset-Rector>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `use-short-assignations <https://github.com/dseguy/clearPHP/tree/master/rules/use-short-assignations.md>`__                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-structures-coulduseshortassignation`, :ref:`case-thelia-structures-coulduseshortassignation`                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


