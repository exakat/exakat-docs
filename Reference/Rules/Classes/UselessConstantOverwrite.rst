.. _classes-uselessconstantoverwrite:


.. _useless-constant-overwrite:

Useless Constant Overwrite
++++++++++++++++++++++++++

.. meta::
	:description:
		Useless Constant Overwrite: A class constant is defined in a parent and child class, with the same value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Constant Overwrite
	:twitter:description: Useless Constant Overwrite: A class constant is defined in a parent and child class, with the same value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Constant Overwrite
	:og:type: article
	:og:description: A class constant is defined in a parent and child class, with the same value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Constant Overwrite.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessConstantOverwrite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessConstantOverwrite.html","name":"Useless Constant Overwrite","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"A class constant is defined in a parent and child class, with the same value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Constant Overwrite.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A class constant is defined in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and child class, with the same value. One of them is useless and may be removed.

.. code-block:: php
   
   <?php
   
   class x {
   	const A = 1;
   	const B = 1;
   }
   
   class y extends x {
   	// A is the same as in the parent class.
   	const A = 1;
   	// B has a new value, so it is important.
   	const B = 2;
   }
   
   ?>
Connex PHP features
-------------------

  + `duplication <https://php-dictionary.readthedocs.io/en/latest/dictionary/duplication.ini.html>`_
  + `Static Constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_
  + `hierarchy <https://php-dictionary.readthedocs.io/en/latest/dictionary/hierarchy.ini.html>`_


Suggestions
___________

* Remove the parent constant
* Remove the child constant




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessConstantOverwrite                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


