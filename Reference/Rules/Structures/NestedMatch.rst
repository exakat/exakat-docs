.. _structures-nestedmatch:

.. _nested-match:

Nested Match
++++++++++++

.. meta::
	:description:
		Nested Match: Nested match calls makes the code difficult to read.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nested Match
	:twitter:description: Nested Match: Nested match calls makes the code difficult to read
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nested Match
	:og:type: article
	:og:description: Nested match calls makes the code difficult to read
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NestedMatch.html
	:og:locale: en
Nested match calls makes the code difficult to read. It is recommended to avoid nesting match calls.

.. code-block:: php
   
   <?php
   
   $a = match($b) {
   	1 => 3,
   	3 => 'ab',
   	5 => match($c) {
   		6 => new X,
   		7 => [],
   	}
   	default => false,
   };
   
   ?>

Suggestions
___________

* Merge the two match() in one.
* Replace the nested match call by a method call.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NestedMatch                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


