.. _dump-typehintorder:

.. _typehint-order:

Typehint Order
++++++++++++++

.. meta::
	:description:
		Typehint Order: Topological order, based on typehints.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Typehint Order
	:twitter:description: Typehint Order: Topological order, based on typehints
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Typehint Order
	:og:type: article
	:og:description: Topological order, based on typehints
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Typehint Order.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/Typehintorder.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/Typehintorder.html","name":"Typehint Order","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Topological order, based on typehints","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Typehint Order.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Topological order, based on typehints. 

Each function, method that use typehint is a link between a type of data and another one. The argument typehint acts as a filter, and the returned type hint is the next step.

.. code-block:: php
   
   <?php
   
   // This library imposes the following order : A -> B -> C 
   function foo(A $a) : B { }
   function bar(B $b) : C { }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/Typehintorder                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                                                                                   |
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


