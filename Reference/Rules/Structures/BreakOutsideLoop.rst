.. _structures-breakoutsideloop:

.. _break-outside-loop:

Break Outside Loop
++++++++++++++++++

.. meta\:\:
	:description:
		Break Outside Loop: Starting with PHP 7, break or continue that are outside a loop (for, foreach(), do.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Break Outside Loop
	:twitter:description: Break Outside Loop: Starting with PHP 7, break or continue that are outside a loop (for, foreach(), do
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Break Outside Loop
	:og:type: article
	:og:description: Starting with PHP 7, break or continue that are outside a loop (for, foreach(), do
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/BreakOutsideLoop.html
	:og:locale: en
  Starting with PHP 7, `break <https://www.php.net/manual/en/control-structures.break.php>`_ or `continue <https://www.php.net/manual/en/control-structures.continue.php>`_ that are outside a loop (for, `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_, do...`while() <https://www.php.net/manual/en/control-structures.while.php>`_, `while()) <https://www.php.net/manual/en/control-structures.while.php>`_ or a `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ statement won't compile anymore.

It is not possible anymore to include a piece of code inside a loop that will then `break <https://www.php.net/manual/en/control-structures.break.php>`_.

.. code-block:: php
   
   <?php
   
       // outside a loop : This won't compile
       break 1; 
       
       foreach($array as $a) {
           break 1; // Compile OK
   
           break 2; // This won't compile, as this break is in one loop, and not 2
       }
   
       foreach($array as $a) {
           foreach($array2 as $a2) {
               break 2; // OK in PHP 5 and 7
           }
       }
   ?>
Connex PHP features
-------------------

  + `break <https://php-dictionary.readthedocs.io/en/latest/dictionary/break.ini.html>`_
  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BreakOutsideLoop                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


