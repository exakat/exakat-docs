.. _php-comparisonondifferenttypes:

.. _comparison-on-different-types:

Comparison On Different Types
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Comparison On Different Types: This rule reports comparisons and spaceship operator that are used with distinct types.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Comparison On Different Types
	:twitter:description: Comparison On Different Types: This rule reports comparisons and spaceship operator that are used with distinct types
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Comparison On Different Types
	:og:type: article
	:og:description: This rule reports comparisons and spaceship operator that are used with distinct types
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Comparison On Different Types.html
	:og:locale: en
This rule reports comparisons and spaceship operator that are used with distinct types. When the types are distinct, PHP apply silent type juggling, and it may `result <https://www.php.net/result>`_ in unexpected results. 

.. code-block:: php
   
   <?php
   
   1 == 'a';
   
   ?>

Suggestions
___________

* Ensure both operands are using the same type.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ComparisonOnDifferentTypes                                                                                          |
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
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


