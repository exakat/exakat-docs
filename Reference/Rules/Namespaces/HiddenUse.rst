.. _namespaces-hiddenuse:

.. _hidden-use-expression:

Hidden Use Expression
+++++++++++++++++++++

.. meta::
	:description:
		Hidden Use Expression: The use expression for namespaces should always be at the beginning of the namespace block.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Hidden Use Expression
	:twitter:description: Hidden Use Expression: The use expression for namespaces should always be at the beginning of the namespace block
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Hidden Use Expression
	:og:type: article
	:og:description: The use expression for namespaces should always be at the beginning of the namespace block
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hidden Use Expression.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/HiddenUse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/HiddenUse.html","name":"Hidden Use Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The use expression for namespaces should always be at the beginning of the namespace block","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hidden Use Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The use expression for namespaces should always be at the beginning of the namespace block. 

It is where everyone expect them, and it is less confusing than having them at various levels.

.. code-block:: php
   
   <?php
   
   // This is visible 
   use A;
   
   class B {}
   
   // This is hidden 
   use C as D;
   
   class E extends D {
       use traitT; // This is a use for a trait
   
       function foo() {
           // This is a use for a closure
           return function ($a) use ($b) {}
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `use <https://php-dictionary.readthedocs.io/en/latest/dictionary/use.ini.html>`_


Suggestions
___________

* Group all uses together, at the beginning of the namespace or class




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/HiddenUse                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tikiwiki-namespaces-hiddenuse`, :ref:`case-openemr-namespaces-hiddenuse`                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


