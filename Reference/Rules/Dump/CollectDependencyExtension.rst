.. _dump-collectdependencyextension:

.. _collect-dependency-extension:

Collect Dependency Extension
++++++++++++++++++++++++++++

.. meta::
	:description:
		Collect Dependency Extension: This analysis lists the interfaces and classes that are not defined in the current code, yet extended.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Dependency Extension
	:twitter:description: Collect Dependency Extension: This analysis lists the interfaces and classes that are not defined in the current code, yet extended
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Dependency Extension
	:og:type: article
	:og:description: This analysis lists the interfaces and classes that are not defined in the current code, yet extended
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Dependency Extension.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectDependencyExtension.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectDependencyExtension.html","name":"Collect Dependency Extension","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This analysis lists the interfaces and classes that are not defined in the current code, yet extended","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Dependency Extension.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This analysis lists the interfaces and classes that are not defined in the current code, yet extended. 

This yields a list of external dependencies. It is useful for anyone who would like to update those root classes and interfaces.

.. code-block:: php
   
   <?php
   
   class MyClass implements \Composer\EventDispatcher\EventSubscriberInterface {
       //..
   }
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectDependencyExtension                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


