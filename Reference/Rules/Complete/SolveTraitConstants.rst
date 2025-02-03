.. _complete-solvetraitconstants:

.. _solve-trait-constants:

Solve Trait Constants
+++++++++++++++++++++

.. meta::
	:description:
		Solve Trait Constants: Adds a link between static constant usage and a class constant set in a trait.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Solve Trait Constants
	:twitter:description: Solve Trait Constants: Adds a link between static constant usage and a class constant set in a trait
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Solve Trait Constants
	:og:type: article
	:og:description: Adds a link between static constant usage and a class constant set in a trait
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Solve Trait Constants.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SolveTraitConstants.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SolveTraitConstants.html","name":"Solve Trait Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Adds a link between static constant usage and a class constant set in a trait","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Solve Trait Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Adds a link between `static <https://www.php.net/manual/en/language.oop5.static.php>`_ constant usage and a class constant set in a trait. 
Constants in traits are added in PHP 8.2.

.. code-block:: php
   
   <?php
   
   trait t { const A = 1; }
   
   class x {
   	use t;
   	
   	function foo() {
   		echo self::A;
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SolveTraitConstants                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


