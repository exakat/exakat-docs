.. _dump-collectclassesdependencies:


.. _collect-classes-dependencies:

Collect Classes Dependencies
++++++++++++++++++++++++++++

.. meta::
	:description:
		Collect Classes Dependencies: This rule collects class dependencies.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Classes Dependencies
	:twitter:description: Collect Classes Dependencies: This rule collects class dependencies
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Classes Dependencies
	:og:type: article
	:og:description: This rule collects class dependencies
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Classes Dependencies.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectClassesDependencies.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectClassesDependencies.html","name":"Collect Classes Dependencies","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule collects class dependencies","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Classes Dependencies.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule collects class dependencies. Each call to one or the other resource put forward by a class creates a link between two points in the code. 

Class dependencies are based on typehint, calls (`static <https://www.php.net/manual/en/language.oop5.static.php>`_ or normal), `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_, catch, attributes, extends. 

The `result <https://www.php.net/result>`_ is a graph of dependencies : some classes depends on others, and vice-versa.

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectClassesDependencies                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Classdependencies <ruleset-Classdependencies>`, :ref:`Dump <ruleset-Dump>`  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


