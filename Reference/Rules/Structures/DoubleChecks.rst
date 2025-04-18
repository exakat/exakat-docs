.. _structures-doublechecks:


.. _double-checks:

Double Checks
+++++++++++++

.. meta::
	:description:
		Double Checks: Double checks happen when data is checked at one point, and then, checked again, with the same test, in a following call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Double Checks
	:twitter:description: Double Checks: Double checks happen when data is checked at one point, and then, checked again, with the same test, in a following call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Double Checks
	:og:type: article
	:og:description: Double checks happen when data is checked at one point, and then, checked again, with the same test, in a following call
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Double Checks.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DoubleChecks.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DoubleChecks.html","name":"Double Checks","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Double checks happen when data is checked at one point, and then, checked again, with the same test, in a following call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Double Checks.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Double checks happen when data is checked at one point, and then, checked again, with the same test, in a following call.

Some of the testing may be pushed to the type system, for example `is_int() <https://www.php.net/is_int>`_ and ``int`` type. Others can't, as the check is not integrated in the type system, such as `is_readable() <https://www.php.net/is_readable>`_ and ``string``, for a path. 

The check may be removed from the method, when the method is not called elsewhere without protection. 
Cleaning such structure leads to micro-optimisation.

.. code-block:: php
   
   <?php
   
   if (is_writeable($path)) {
   	foo($path);
   }
   
   function foo(string $path) {
   	// This was already tested
   	if (!is_writeable($path)) {
   		return;
   	}
   }
   
   ?>

Suggestions
___________

* Remove the check in the method
* Remove the check in the caller code
* Use type system




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DoubleChecks                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
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


