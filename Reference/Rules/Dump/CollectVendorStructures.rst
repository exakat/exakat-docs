.. _dump-collectvendorstructures:


.. _collect-vendor-structures:

Collect Vendor Structures
+++++++++++++++++++++++++


.. meta::

	:description:

		Collect Vendor Structures: Collect the structures (constant, function, classes, interfaces, traits, enums, .

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Collect Vendor Structures

	:twitter:description: Collect Vendor Structures: Collect the structures (constant, function, classes, interfaces, traits, enums, 

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Collect Vendor Structures

	:og:type: article

	:og:description: Collect the structures (constant, function, classes, interfaces, traits, enums, 

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Vendor Structures.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectVendorStructures.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectVendorStructures.html","name":"Collect Vendor Structures","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Collect the structures (constant, function, classes, interfaces, traits, enums, ","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Vendor Structures.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Collect the structures (constant, function, classes, interfaces, traits, enums, `...) <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ that are defined as stubs in the configuration.

+----------+---------+------+---------------------------------------------------------------------------------------------------------+
| Name     | Default | Type | Description                                                                                             |
+----------+---------+------+---------------------------------------------------------------------------------------------------------+
| pdffList | []      | json | List of vendors, their version and related PDFF. {'vendor':['wordpress.5.9.pdff','wordpress.5.8.pdff']} |
+----------+---------+------+---------------------------------------------------------------------------------------------------------+



Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectVendorStructures                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


