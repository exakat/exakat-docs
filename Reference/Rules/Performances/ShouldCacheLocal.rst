.. _performances-shouldcachelocal:


.. _should-cache-local:

Should Cache Local
++++++++++++++++++

.. meta::
	:description:
		Should Cache Local: Repeated calls to a method with the same arguments should be put in a local cache.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Cache Local
	:twitter:description: Should Cache Local: Repeated calls to a method with the same arguments should be put in a local cache
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Cache Local
	:og:type: article
	:og:description: Repeated calls to a method with the same arguments should be put in a local cache
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Cache Local.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ShouldCacheLocal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ShouldCacheLocal.html","name":"Should Cache Local","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Repeated calls to a method with the same arguments should be put in a local cache","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Cache Local.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Repeated calls to a method with the same arguments should be put in a local cache. 

It speeds up processing, even in case of a simple property fetch. A local cache makes the code more readable and more compact.

.. code-block:: php
   
   <?php
   
   function foo() {
   	$goo = goo(), 0, 3;
   	$a = strtolower($goo);
   	$b = strtoupper($goo);
   	
   	return $a . '-' . $b;
   }
   
   function foo2() {
   	$a = strtolower(goo(), 0, 3);
   	$b = strtoupper(goo(), 0, 3);
   	
   	return $a . '-' . $b;
   }
   
   ?>
Connex PHP features
-------------------

  + `Micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Suggestions
___________

* Use a local cache to reduce processing time




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/ShouldCacheLocal                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


