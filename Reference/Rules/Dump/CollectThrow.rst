.. _dump-collectthrow:

.. _collect-throw-calls:

Collect Throw Calls
+++++++++++++++++++

.. meta::
	:description:
		Collect Throw Calls: This rule collects all `throw` command usage, along with the exception thrown and the calling method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Throw Calls
	:twitter:description: Collect Throw Calls: This rule collects all `throw` command usage, along with the exception thrown and the calling method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Throw Calls
	:og:type: article
	:og:description: This rule collects all `throw` command usage, along with the exception thrown and the calling method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Throw Calls.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectThrow.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectThrow.html","name":"Collect Throw Calls","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule collects all `throw` command usage, along with the exception thrown and the calling method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Throw Calls.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rule collects all `throw` command usage, along with the `exception <https://www.php.net/exception>`_ thrown and the calling method.

.. code-block:: php
   
   <?php
   
   function foo() {
   	throw Exception();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectThrow                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
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


