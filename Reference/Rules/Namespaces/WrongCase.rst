.. _namespaces-wrongcase:


.. _wrong-case-namespaces:

Wrong Case Namespaces
+++++++++++++++++++++

.. meta::
	:description:
		Wrong Case Namespaces: Namespaces are case-insensitive.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Case Namespaces
	:twitter:description: Wrong Case Namespaces: Namespaces are case-insensitive
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Case Namespaces
	:og:type: article
	:og:description: Namespaces are case-insensitive
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Case Namespaces.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/WrongCase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/WrongCase.html","name":"Wrong Case Namespaces","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Namespaces are case-insensitive","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Case Namespaces.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Namespaces are case-insensitive.

.. code-block:: php
   
   <?php
   
   // Namespaces should share the same case
   namespace X {}
   
   namespace x {}
   
   ?>
Connex PHP features
-------------------

  + `Namespaces <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_


Suggestions
___________

* Synchronize all names 




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/WrongCase                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


