.. _complete-returntypehint:


.. _add-return-type:

Add Return Type
+++++++++++++++

.. meta::
	:description:
		Add Return Type: Add returntype to methods, functions, closures and arrow functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Add Return Type
	:twitter:description: Add Return Type: Add returntype to methods, functions, closures and arrow functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Add Return Type
	:og:type: article
	:og:description: Add returntype to methods, functions, closures and arrow functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Add Return Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/ReturnTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/ReturnTypehint.html","name":"Add Return Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"Add returntype to methods, functions, closures and arrow functions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Add Return Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Add returntype to methods, functions, closures and arrow functions. The return types are read from the code and deduced, based on literal values, local types and operations.

.. code-block:: php
   
   <?php
   
   // This has no type, but could use int
   function foo() {
       return 1;
   }
   
   // This has no type, but could use string
   function goo(string $a) {
       return $a;
   }
   
   // This has no type, but could use string
   function hoo($a) {
       return $a - 2;
   }
   
   ?>

Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/ReturnTypehint                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`First <ruleset-First>`, :ref:`NoDoc <ruleset-NoDoc>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


