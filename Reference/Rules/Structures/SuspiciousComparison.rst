.. _structures-suspiciouscomparison:

.. _suspicious-comparison:

Suspicious Comparison
+++++++++++++++++++++

.. meta::
	:description:
		Suspicious Comparison: The comparison seems to be misplaced.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Suspicious Comparison
	:twitter:description: Suspicious Comparison: The comparison seems to be misplaced
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Suspicious Comparison
	:og:type: article
	:og:description: The comparison seems to be misplaced
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Suspicious Comparison.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SuspiciousComparison.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SuspiciousComparison.html","name":"Suspicious Comparison","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The comparison seems to be misplaced","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Suspicious Comparison.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The comparison seems to be misplaced.

A comparison happens in the last argument, while the actual function expect another type : this may be the case of a badly placed parenthesis.
Original idea by `Vladimir Reznichenko <https://twitter.com/kalessil>`_.

.. code-block:: php
   
   <?php
   
   // trim expect a string, a boolean is given.
   if (trim($str === '')){
   
   }
   
   // Just move the first closing parenthesis to give back its actual meaning
   if (trim($str) === ''){
   
   }
   
   ?>
Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Remove the comparison altogether
* Move the comparison to its right place : that, or more the parenthesis.
* This may be what is intended : just leave it.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SuspiciousComparison                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpipam-structures-suspiciouscomparison`, :ref:`case-expressionengine-structures-suspiciouscomparison`       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


