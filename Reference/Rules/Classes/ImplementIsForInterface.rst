.. _classes-implementisforinterface:


.. _implements-is-for-interface:

Implements Is For Interface
+++++++++++++++++++++++++++

.. meta::
	:description:
		Implements Is For Interface: With class heritage, implements should be used for interfaces, and extends with classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Implements Is For Interface
	:twitter:description: Implements Is For Interface: With class heritage, implements should be used for interfaces, and extends with classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Implements Is For Interface
	:og:type: article
	:og:description: With class heritage, implements should be used for interfaces, and extends with classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Implements Is For Interface.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ImplementIsForInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ImplementIsForInterface.html","name":"Implements Is For Interface","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"With class heritage, implements should be used for interfaces, and extends with classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Implements Is For Interface.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

With class heritage, implements should be used for interfaces, and extends with classes.

PHP defers the implements check until execution : the code in example does lint, but won,t run.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {}
   }
   
   interface y {
       function foo();
   }
   
   // Use implements with an interface
   class z implements y {}
   
   // Implements is for an interface, not a class
   class z implements x {}
   
   ?>
Related PHP errors 
-------------------

  + `%s cannot implement %s - it is not an interface <https://php-errors.readthedocs.io/en/latest/messages/%25s-cannot-implement-%25s---it-is-not-an-interface.html>`_



Connex PHP features
-------------------

  + `implements <https://php-dictionary.readthedocs.io/en/latest/dictionary/implements.ini.html>`_
  + `Interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Create an interface from the class, and use it with the implements keyword




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ImplementIsForInterface                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


