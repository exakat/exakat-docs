.. _structures-oneexpressionbracketsconsistency:


.. _one-expression-brackets-consistency:

One Expression Brackets Consistency
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		One Expression Brackets Consistency: Brackets around one-line expressions are not consistent.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: One Expression Brackets Consistency
	:twitter:description: One Expression Brackets Consistency: Brackets around one-line expressions are not consistent
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: One Expression Brackets Consistency
	:og:type: article
	:og:description: Brackets around one-line expressions are not consistent
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/One Expression Brackets Consistency.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OneExpressionBracketsConsistency.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OneExpressionBracketsConsistency.html","name":"One Expression Brackets Consistency","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Brackets around one-line expressions are not consistent","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/One Expression Brackets Consistency.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Brackets around one-line expressions are not consistent. 

PHP makes bracket optional when a control structure pilot only one expression. Both are semantically identical.

This analysis reports code that uses brackets while the vast majority of other expressions uses none. Or the contrary. 
Another analysis, [Structures/Bracketless], reports the absence of brackets as an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // One expression with brackets
   for($i = 0; $i < 10; $i++) { $c++; }
   
   // One expression without bracket
   for($i2 = 0; $i2 < 10; $i2++)  $c++; 
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneExpressionBracketsConsistency                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


