.. _structures-wrongrange:


.. _unreadable-interval-check:

Unreadable Interval Check
+++++++++++++++++++++++++

.. meta::
	:description:
		Unreadable Interval Check: When checking that a value belongs to a certain interval, the interval check should use && and not ||.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unreadable Interval Check
	:twitter:description: Unreadable Interval Check: When checking that a value belongs to a certain interval, the interval check should use && and not ||
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unreadable Interval Check
	:og:type: article
	:og:description: When checking that a value belongs to a certain interval, the interval check should use && and not ||
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unreadable Interval Check.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WrongRange.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WrongRange.html","name":"Unreadable Interval Check","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"When checking that a value belongs to a certain interval, the interval check should use && and not ||","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unreadable Interval Check.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When checking that a value belongs to a certain interval, the interval check should use && and not ||.

The expression should be read that ``$a`` is greater than a lower limit and lesser than an upper limit. 

Expressions with ``||`` are less readable: they should be build that ``$a`` is below a lower limit, or beyond an upper limit, and that triggers the `error <https://www.php.net/error>`_.


.. code-block:: php
   
   <?php
   
   //interval correctly checked a is between 2 and 999
   if ($a > 1 && $a < 1000) {}
   
   //interval incorrectly checked : a is 2 or more ($a < 1000 is never checked)
   if ($a > 1 || $a < 1000) {}
   
   ?>

Suggestions
___________

* Make the interval easy to read and understand
* Check the truth table for the logical operation




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/WrongRange                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-wrongrange`, :ref:`case-wordpress-structures-wrongrange`                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


