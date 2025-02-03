.. _classes-couldbeiterable:


.. _this-could-be-iterable:

This Could Be Iterable
++++++++++++++++++++++

.. meta::
	:description:
		This Could Be Iterable: An argument that is both array and traversable may be typed iterable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: This Could Be Iterable
	:twitter:description: This Could Be Iterable: An argument that is both array and traversable may be typed iterable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: This Could Be Iterable
	:og:type: article
	:og:description: An argument that is both array and traversable may be typed iterable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/This Could Be Iterable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeIterable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeIterable.html","name":"This Could Be Iterable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"An argument that is both array and traversable may be typed iterable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/This Could Be Iterable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

An argument that is both array and `traversable <https://www.php.net/`traversable <https://www.php.net/traversable>`_>`_ may be typed iterable. Iterable is a more generic type than array, and allows the usage of iterators too.

.. code-block:: php
   
   <?php
   
   // parameter and return type might be iterable
   function foo($a) {
       foreach($a as $b) {
       	// do something
       }
       
       return $a;
   }
   
   class x {
   	private $b;
   	
   	function foo() {
       	foreach($this->b as $c) {
       		// do something
   	    }
   	}
   }
   
   ?>

See also `iterable <https://www.php.net/manual/en/language.types.iterable.php>`_.

Connex PHP features
-------------------

  + `iterable <https://php-dictionary.readthedocs.io/en/latest/dictionary/iterable.ini.html>`_


Suggestions
___________

* Add the iterable typehint




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeIterable                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and more recent                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+


