.. _structures-shortorcompletecomparison:


.. _short-or-complete-comparison:

Short Or Complete Comparison
++++++++++++++++++++++++++++

.. meta::
	:description:
		Short Or Complete Comparison: Which type of condition is used for boolean comparisons : either short or formal.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Short Or Complete Comparison
	:twitter:description: Short Or Complete Comparison: Which type of condition is used for boolean comparisons : either short or formal
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Short Or Complete Comparison
	:og:type: article
	:og:description: Which type of condition is used for boolean comparisons : either short or formal
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Short Or Complete Comparison.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShortOrCompleteComparison.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShortOrCompleteComparison.html","name":"Short Or Complete Comparison","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Which type of condition is used for boolean comparisons : either short or formal","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Short Or Complete Comparison.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Which type of condition is used for boolean comparisons : either short or formal. 

Formal is an explicit comparison to another boolean, while short is when the variable is used without comparison. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   // returns a boolean
   $checked = checkSomething(); 
   
   // short comparison
   if ($checked) {
   	// doSomething()
   }
   
   // also short comparison
   if (!$checked) {
   	// doSomething()
   }
   
   // formal comparison
   if ($checked === true) {
   	// doSomething()
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShortOrCompleteComparison                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


