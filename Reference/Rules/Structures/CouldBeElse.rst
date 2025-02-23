.. _structures-couldbeelse:


.. _could-be-else:

Could Be Else
+++++++++++++

.. meta::
	:description:
		Could Be Else: Merge opposite conditions into one if/then structure.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Else
	:twitter:description: Could Be Else: Merge opposite conditions into one if/then structure
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Else
	:og:type: article
	:og:description: Merge opposite conditions into one if/then structure
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Else.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeElse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeElse.html","name":"Could Be Else","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Merge opposite conditions into one if\/then structure","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Else.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Merge opposite conditions into one if/then structure.

When two if/then structures follow each other, using a condition and its opposite, they may be merged into one.

.. code-block:: php
   
   <?php
   
   // Short version
   if ($a == 1) {
       $b = 2;
   } else {
       $b = 1;
   }
   
   // Long version
   if ($a == 1) {
       $b = 2;
   }
   
   if ($a != 1) {
       $b = 3;
   }
   
   ?>
Connex PHP features
-------------------

  + `If Then Else <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Merge the two conditions into one structure
* Check if the second condition is still applicable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeElse                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-structures-couldbeelse`, :ref:`case-openemr-structures-couldbeelse`                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


