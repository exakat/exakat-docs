.. _structures-wrongrange:

.. _wrong-range-check:

Wrong Range Check
+++++++++++++++++

.. meta::
	:description:
		Wrong Range Check: The interval check should use && and not ||.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Range Check
	:twitter:description: Wrong Range Check: The interval check should use && and not ||
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Range Check
	:og:type: article
	:og:description: The interval check should use && and not ||
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Range Check.html
	:og:locale: en
The interval check should use && and not ||.

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


