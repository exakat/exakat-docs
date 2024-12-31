.. _structures-breaknoninteger:

.. _break-with-non-integer:

Break With Non Integer
++++++++++++++++++++++

.. meta\:\:
	:description:
		Break With Non Integer: When using a break, the argument of the operator must be a positive non-null integer literal or be omitted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Break With Non Integer
	:twitter:description: Break With Non Integer: When using a break, the argument of the operator must be a positive non-null integer literal or be omitted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Break With Non Integer
	:og:type: article
	:og:description: When using a break, the argument of the operator must be a positive non-null integer literal or be omitted
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/BreakNonInteger.html
	:og:locale: en
  When using a `break <https://www.php.net/manual/en/control-structures.break.php>`_, the argument of the operator must be a positive non-null integer literal or be omitted.

Other values were acceptable in PHP 5.3 and previous version, but this is now reported as an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
       // Can't break $a, even if it contains an integer.
       $a = 1;
       for($i = 0; $i < 10; $i++) {
           break $a;
       }
   
       // can't break on float
       for($i = 0; $i < 10; $i++) {
           for($j = 0; $j < 10; $j++) {
               break 2.2;
           }
       }
   
   ?>

Suggestions
___________

* Only use integer with break




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BreakNonInteger                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


