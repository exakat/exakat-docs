.. _classes-strangename:

.. _strange-names-in-classes:

Strange Names In Classes
++++++++++++++++++++++++

.. meta::
	:description:
		Strange Names In Classes: Those methods, properties, constants or types should have another name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strange Names In Classes
	:twitter:description: Strange Names In Classes: Those methods, properties, constants or types should have another name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strange Names In Classes
	:og:type: article
	:og:description: Those methods, properties, constants or types should have another name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strange Names In Classes.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StrangeName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StrangeName.html","name":"Strange Names In Classes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those methods, properties, constants or types should have another name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Strange Names In Classes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those methods, properties, constants or types should have another name.

Ever wondered why the ``__constructor`` is never called? Or the ``__consturct`` ? 

Those errors most often originate from typos, or quick fixes that where not fully tested. Other times, they were badly chosen, or ran into PHP's own reserved keywords.

.. code-block:: php
   
   <?php
   
   class foo {
       // The real constructor
       function __construct() {}
   
       // The fake constructor
       function __constructor() {}
       
       // The 'typo'ed' constructor
       function __consturct() {}
       
       // This doesn't clone
       function clone() {}
   }
   
   ?>

Suggestions
___________

* Use the proper name
* Remove the method, when it is not used and tests still pass.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StrangeName                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.1                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


