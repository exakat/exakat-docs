.. _interfaces-emptyinterface:


.. _empty-interfaces:

Empty Interfaces
++++++++++++++++

.. meta::
	:description:
		Empty Interfaces: Empty interfaces are a code smell.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Interfaces
	:twitter:description: Empty Interfaces: Empty interfaces are a code smell
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Interfaces
	:og:type: article
	:og:description: Empty interfaces are a code smell
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Interfaces.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/EmptyInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/EmptyInterface.html","name":"Empty Interfaces","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Empty interfaces are a code smell","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Empty Interfaces.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Empty interfaces are a code smell. Interfaces should contains at least a method or a constant, and not be totally empty.

.. code-block:: php
   
   <?php
   
   // an empty interface
   interface empty {}
   
   // an normal interface
   interface normal {
       public function i() ;
   }
   
   // a constants interface
   interface constantsOnly {
       const FOO = 1;
   }
   
   ?>

See also `Empty interfaces are bad practice <https://r.je/empty-interfaces-bad-practice.html>`_ and `Blog : Are empty interfaces code smell? <https://hackernoon.com/are-interfaces-code-smell-bd19abc266d3>`_.

Connex PHP features
-------------------

  + `Interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Remove the interface
* Add some methods or constants to the interface




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/EmptyInterface                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


