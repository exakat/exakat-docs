.. _structures-repeatedregex:

.. _repeated-regex:

Repeated Regex
++++++++++++++

.. meta::
	:description:
		Repeated Regex: Repeated regex should be centralized.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Repeated Regex
	:twitter:description: Repeated Regex: Repeated regex should be centralized
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Repeated Regex
	:og:type: article
	:og:description: Repeated regex should be centralized
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Repeated Regex.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RepeatedRegex.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RepeatedRegex.html","name":"Repeated Regex","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Repeated regex should be centralized","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Repeated Regex.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Repeated regex should be centralized. 

When a regex is repeatedly used in the code, it is getting harder to update. 
Regex that are repeated at least once (aka, used twice or more) are reported. Regex that are dynamically build are not reported.

.. code-block:: php
   
   <?php
   
   // Regex used several times, at least twice.
   preg_match('/^abc_|^square$/i', $_GET['x']);
   
   //.......
   
   preg_match('/^abc_|^square$/i', $row['name']);
   
   // This regex is dynamically built, so it is not reported.
   preg_match('/^circle|^'.$x.'$/i', $string);
   
   // This regex is used once, so it is not reported.
   preg_match('/^circle|^square$/i', $string);
   
   ?>
Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Create a central library of regex
* Use the regex inventory to spot other regex that are close, and should be identical.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RepeatedRegex                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.9                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-vanilla-structures-repeatedregex`, :ref:`case-tikiwiki-structures-repeatedregex`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


