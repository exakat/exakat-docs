.. _classes-multiplepropertydeclarationononeline:

.. _multiple-property-declaration-on-one-line:

Multiple Property Declaration On One Line
+++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Property Declaration On One Line: Multiple properties are defined on the same line.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Property Declaration On One Line
	:twitter:description: Multiple Property Declaration On One Line: Multiple properties are defined on the same line
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Property Declaration On One Line
	:og:type: article
	:og:description: Multiple properties are defined on the same line
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Property Declaration On One Line.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MultiplePropertyDeclarationOnOneLine.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MultiplePropertyDeclarationOnOneLine.html","name":"Multiple Property Declaration On One Line","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Multiple properties are defined on the same line","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Property Declaration On One Line.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Multiple properties are defined on the same line. They could be defined independently, on separate expressions.

Keeping properties separate helps documenting and refactoring them independently.

.. code-block:: php
   
   <?php
   
   // multiple definition on one expression
   class point {
       private $x, $y, $z;
   
       // more code
   }
   
   // one line, one definition
   class point2 {
       private $x;
       
       private $y;
       
       private $z;
   
       // more code
   }
   
   ?>

Suggestions
___________

* Split the definitions to one by line




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MultiplePropertyDeclarationOnOneLine                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                                |
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


