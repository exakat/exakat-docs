.. _structures-coulduseyieldfrom:


.. _could-use-yield-from:

Could Use Yield From
++++++++++++++++++++

.. meta::
	:description:
		Could Use Yield From: ``Yield from`` can be applied to an array or another generator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Yield From
	:twitter:description: Could Use Yield From: ``Yield from`` can be applied to an array or another generator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Yield From
	:og:type: article
	:og:description: ``Yield from`` can be applied to an array or another generator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Yield From.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseYieldFrom.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseYieldFrom.html","name":"Could Use Yield From","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"``Yield from`` can be applied to an array or another generator","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Yield From.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``Yield from`` can be applied to an array or another `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_. It replaces a loop and a ``yield`` call. The resulting syntax is shorter and faster.

.. code-block:: php
   
   <?php
   
   foreach(foo() as $f) {
   	doSomething($f);
   }
   
   // using yield and a loop to yield all elements  
   function foo() {
   	foreach(goo() as $g) {
   		yield $g;
   	}
   }
   
   // using yield from to yield all elements  
   function foo2() {
   	yield from goo();
   }
   
   function goo() : array {
   	return [1,2,3];
   }
   
   ?>
Connex PHP features
-------------------

  + `yield from Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_


Suggestions
___________

* Use ``yield from`` keyword and shorten the syntax




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseYieldFrom                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


