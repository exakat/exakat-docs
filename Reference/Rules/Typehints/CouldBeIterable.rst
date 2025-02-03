.. _typehints-couldbeiterable:

.. _typehint-could-be-iterable:

Typehint Could Be Iterable
++++++++++++++++++++++++++

.. meta::
	:description:
		Typehint Could Be Iterable: Mark arguments, class constants, properties and return types that can be set to ``iterable``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Typehint Could Be Iterable
	:twitter:description: Typehint Could Be Iterable: Mark arguments, class constants, properties and return types that can be set to ``iterable``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Typehint Could Be Iterable
	:og:type: article
	:og:description: Mark arguments, class constants, properties and return types that can be set to ``iterable``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Typehint Could Be Iterable.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldBeIterable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldBeIterable.html","name":"Typehint Could Be Iterable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark arguments, class constants, properties and return types that can be set to ``iterable``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Typehint Could Be Iterable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Mark arguments, class constants, properties and return types that can be set to ``iterable``.

.. code-block:: php
   
   <?php
   
   // Accept an array or a traversable Object as input 
   function foo($b) {
       foreach($b as $c) {
       
       }
   
       // Returns an array
       return [$b];
   }
   
   ?>
Connex PHP features
-------------------

  + `iterable <https://php-dictionary.readthedocs.io/en/latest/dictionary/iterable.ini.html>`_


Suggestions
___________

* Add `iterable` typehint to the code (PHP 8.0+).




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeIterable                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Typechecks <ruleset-Typechecks>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


