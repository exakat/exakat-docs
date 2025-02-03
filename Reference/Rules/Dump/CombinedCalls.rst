.. _dump-combinedcalls:

.. _combined-calls:

Combined Calls
++++++++++++++

.. meta::
	:description:
		Combined Calls: This collects all the combined function or method calls.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Combined Calls
	:twitter:description: Combined Calls: This collects all the combined function or method calls
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Combined Calls
	:og:type: article
	:og:description: This collects all the combined function or method calls
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Combined Calls.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CombinedCalls.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CombinedCalls.html","name":"Combined Calls","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This collects all the combined function or method calls","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Combined Calls.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This collects all the combined function or method calls. Those are methods that are called in succession.

.. code-block:: php
   
   <?php
   
   $a = ucfirst(strtolower($name));
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CombinedCalls                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                   |
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


