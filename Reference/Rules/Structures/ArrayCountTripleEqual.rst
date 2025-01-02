.. _structures-arraycounttripleequal:

.. _empty-array-detection:

Empty Array Detection
+++++++++++++++++++++

.. meta::
	:description:
		Empty Array Detection: Empty arrays may be detected with different solutions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Array Detection
	:twitter:description: Empty Array Detection: Empty arrays may be detected with different solutions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Array Detection
	:og:type: article
	:og:description: Empty arrays may be detected with different solutions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Array Detection.html
	:og:locale: en
Empty arrays may be detected with different solutions. 
This analysis includes comparison to 0 with count, with ==, ===, != and !==, and comparison to empty arrays. Constants are not handled.

.. code-block:: php
   
   <?php
   
   // comparison to empty array
   $array === [];
   
   // comparison of count() 
   count($array) === 0;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayCountTripleEqual                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
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


