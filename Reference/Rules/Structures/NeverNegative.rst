.. _structures-nevernegative:

.. _always-positive-comparison:

Always Positive Comparison
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Always Positive Comparison: Some PHP native functions, such as count(), strlen(), or abs() only returns positive or null values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Always Positive Comparison
	:twitter:description: Always Positive Comparison: Some PHP native functions, such as count(), strlen(), or abs() only returns positive or null values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Always Positive Comparison
	:og:type: article
	:og:description: Some PHP native functions, such as count(), strlen(), or abs() only returns positive or null values
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NeverNegative.html
	:og:locale: en
  Some PHP native functions, such as `count() <https://www.php.net/count>`_, `strlen() <https://www.php.net/strlen>`_, or `abs() <https://www.php.net/abs>`_ only returns positive or null values. 

When comparing their `result <https://www.php.net/result>`_ to 0, the following expressions are always true and should be avoided.

.. code-block:: php
   
   <?php
   
   $a = [1, 2, 3];
   
   // OK, count() may return 0 or more 
   var_dump(count($a) >= 0);
   
   // This is always false
   var_dump(count($a) < 0); 
   
   ?>

Suggestions
___________

* Compare count() to non-zero values
* Use empty()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NeverNegative                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-structures-nevernegative`                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


