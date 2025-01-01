.. _structures-break0:

.. _break-with-0:

Break With 0
++++++++++++

.. meta::
	:description:
		Break With 0: It is not possible to break 0 : it makes no sense.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Break With 0
	:twitter:description: Break With 0: It is not possible to break 0 : it makes no sense
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Break With 0
	:og:type: article
	:og:description: It is not possible to break 0 : it makes no sense
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/Break0.html
	:og:locale: en
It is not possible to `break <https://www.php.net/manual/en/control-structures.break.php>`_ 0 : it makes no sense. `Break <https://www.php.net/manual/en/control-structures.break.php>`_ 1 is the minimum, and is the default value.

.. code-block:: php
   
   <?php
       // Can't break 0. Must be 1 or more, depending on the level of nesting.
       for($i = 0; $i < 10; $i++) {
           break 0;
       }
   
       for($i = 0; $i < 10; $i++) {
           for($j = 0; $j < 10; $j++) {
               break 2;
           }
       }
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/%27break%27+operator+accepts+only+positive+integers.html>`_




Suggestions
___________

* Remove 0, or the break




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Break0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>` |
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


