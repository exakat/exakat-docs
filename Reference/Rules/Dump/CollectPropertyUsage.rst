.. _dump-collectpropertyusage:


.. _collect-property-usage:

Collect Property Usage
++++++++++++++++++++++


.. meta::

	:description:

		Collect Property Usage: Collect the level of usage of a property.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Collect Property Usage

	:twitter:description: Collect Property Usage: Collect the level of usage of a property

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Collect Property Usage

	:og:type: article

	:og:description: Collect the level of usage of a property

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Property Usage.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectPropertyUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectPropertyUsage.html","name":"Collect Property Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 03 Feb 2025 17:19:52 +0000","dateModified":"Mon, 03 Feb 2025 17:19:52 +0000","description":"Collect the level of usage of a property","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Property Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Collect the level of usage of a property. A property is used in distinct methods. The level of usage is the ratio between the number of methods in which the property is used, divided by the number of total methods. 

In the example below, ``$p`` is used once. ``$q`` is used in two methods, while being used three times in total. 

The level of usage of ``$p`` is now 1 / 2 = 0.5; The level of usage of ``$q`` is now 2 / 2 = 1.

.. code-block:: php
   
   <?php
   
   class x {
   	private $p, $q;
   	
   	function foo() {
   		$this->p = 1;
   		$this->q = 1;
   	}
   
   	function goo() {
   		$this->q = 2;
   		$this->q = 3;
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectPropertyUsage                                                                                               |
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


