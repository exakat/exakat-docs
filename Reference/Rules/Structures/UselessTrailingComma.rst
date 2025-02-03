.. _structures-uselesstrailingcomma:


.. _useless-trailing-comma:

Useless Trailing Comma
++++++++++++++++++++++


.. meta::

	:description:

		Useless Trailing Comma: Trailing comma is the last comma in a call or function definition.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Useless Trailing Comma

	:twitter:description: Useless Trailing Comma: Trailing comma is the last comma in a call or function definition

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Useless Trailing Comma

	:og:type: article

	:og:description: Trailing comma is the last comma in a call or function definition

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Trailing Comma.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessTrailingComma.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessTrailingComma.html","name":"Useless Trailing Comma","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Trailing comma is the last comma in a call or function definition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Trailing Comma.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Trailing comma is the last comma in a call or function definition. It is left with an empty slot aftewards, so as to reduce the diff when adding or removing an element. 

Trailing commas appear in array definition, method calls, method definitions, including use expression for closures and use call. 

Trailing comma with only one element are reported as useless. Then, for multiple elements, the elements should be on separate lines.

This is a coding convention.

.. code-block:: php
   
   <?php
   
   $good = array(1,
   			  2,
   			  3,
   			  4,
   			  );
   
   // The trailing comma is just useless.
   $bad = array( 1, 2, 3, 4, );
   
   ?>
Connex PHP features
-------------------

  + `trailing-comma <https://php-dictionary.readthedocs.io/en/latest/dictionary/trailing-comma.ini.html>`_


Suggestions
___________

* Remove the trailing comma
* Put the trailing comma on a new line




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessTrailingComma                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


