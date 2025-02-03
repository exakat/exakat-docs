.. _classes-propertymethodsamename:


.. _same-name-for-property-and-method:

Same Name For Property And Method
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Same Name For Property And Method: A property and a method have the same name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Same Name For Property And Method
	:twitter:description: Same Name For Property And Method: A property and a method have the same name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Same Name For Property And Method
	:og:type: article
	:og:description: A property and a method have the same name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Same Name For Property And Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyMethodSameName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyMethodSameName.html","name":"Same Name For Property And Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"A property and a method have the same name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Same Name For Property And Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A property and a method have the same name. While it is a valid naming scheme with PHP, it may lead to confusion while codeing. 

Such naming collision may appear with words that are the same as a verb (for method) and as a noun (for property). For example, in English : query, work, debug, run, process, rain, polish, paint, etc,. 

It may also happen during the life cycle of the class, as it is extended with new methods and properties, and little care is give to semantic meaning of the names, beyond the task at hand. 

It is recommended to avoid those collisions, and keep properties and methods named distinctly. 

That problem do not happen to constants, which are mostly written uppercase. This rule is case-insensitive.

.. code-block:: php
   
   <?php
   
   class x {
       public $foo;
       function foo() {}
   }
   
   $x = new X:
   $x->p = $x->foo();
   
   ?>

See also `Words That Are Both Nouns And Verbs <https://www.enchantedlearning.com/wordlist/nounandverb.shtml>`_.

Connex PHP features
-------------------

  + `name <https://php-dictionary.readthedocs.io/en/latest/dictionary/name.ini.html>`_


Suggestions
___________

* Fix any spelling in the names
* Rename the property or the method




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyMethodSameName                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


