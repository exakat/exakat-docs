.. _interfaces-unusedinterfaces:


.. _unused-interfaces:

Unused Interfaces
+++++++++++++++++

.. meta::
	:description:
		Unused Interfaces: Those interfaces are defined and never used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Interfaces
	:twitter:description: Unused Interfaces: Those interfaces are defined and never used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Interfaces
	:og:type: article
	:og:description: Those interfaces are defined and never used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Interfaces.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/UnusedInterfaces.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/UnusedInterfaces.html","name":"Unused Interfaces","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those interfaces are defined and never used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Interfaces.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those interfaces are defined and never used. They should be removed, as they are dead code.

Interfaces may be use as `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ for other interfaces, as types (argument, return and property), in instance of.

.. code-block:: php
   
   <?php
   
   interface used {}
   interface unused {}
   
   // Used by implementation
   class c implements used {}
   
   // Used by extension
   interface j implements used {}
   
   $x = new c;
   
   // Used in a instanceof
   var_dump($x instanceof used); 
   
   // Used in a type
   function foo(Used $x) {}
   
   ?>
Connex PHP features
-------------------

  + `Interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Remove the interface
* Actually use the interface




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/UnusedInterfaces                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-interfaces-unusedinterfaces`                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+


