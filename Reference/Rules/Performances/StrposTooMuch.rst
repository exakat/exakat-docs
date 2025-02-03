.. _performances-strpostoomuch:


.. _strpos()-too-much:

strpos() Too Much
+++++++++++++++++

.. meta::
	:description:
		strpos() Too Much: strpos() covers the whole string before reporting 0.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: strpos() Too Much
	:twitter:description: strpos() Too Much: strpos() covers the whole string before reporting 0
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: strpos() Too Much
	:og:type: article
	:og:description: strpos() covers the whole string before reporting 0
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/strpos() Too Much.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/StrposTooMuch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/StrposTooMuch.html","name":"strpos() Too Much","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"strpos() covers the whole string before reporting 0","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/strpos() Too Much.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`strpos() <https://www.php.net/strpos>`_ covers the whole string before reporting 0. If the expected string is expected be at the beginning, or a fixed place, it is more stable to use `substr() <https://www.php.net/substr>`_ for comparison.

The longer the haystack (the searched string), the more efficient is that trick. The string has to be 10k or more to have impact, unless it is in a loop. 
This applies to `stripos() <https://www.php.net/stripos>`_ too.

.. code-block:: php
   
   <?php
   
   // This always reads the same amount of string
   if (substr($html, 0, 6) === '<html>') {
   
   }
   
   // When searching for a single character, checking with a known position ($string[$position]) is even faster
   if ($html[0] === '<') {
   
   }
   
   // With strpos(), the best way is to search for something that exist, and use absence as worst case scenario 
   if (strpos($html, '<html>') > 0) {
   
   } else {
       // 
   }
   
   // When the search fails, the whole string has been read
   if (strpos($html, '<html>') === 0) {
   
   }
   
   ?>

Suggestions
___________

* Check for presence, and not for absence
* Use substr() and compare the extracted string
* For single chars, try using the position in the string




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/StrposTooMuch                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-performances-strpostoomuch`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


