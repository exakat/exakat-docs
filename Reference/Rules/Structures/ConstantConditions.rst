.. _structures-constantconditions:

.. _constant-conditions:

Constant Conditions
+++++++++++++++++++

.. meta::
	:description:
		Constant Conditions: If/then structures that have constant condition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Conditions
	:twitter:description: Constant Conditions: If/then structures that have constant condition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Conditions
	:og:type: article
	:og:description: If/then structures that have constant condition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constant Conditions.html
	:og:locale: en
If/then structures that have constant condition. 

The condition doesn't change during execution, and the following blocks are always executed or not. This may also lead to an infinite or a null loop. 

When this is the case, the condition may be removed, and dead code may be removed. 
It is advised to remove them, or to make them depend on configuration.

.. code-block:: php
   
   <?php
   
   // static if
   if (0.8) {
       $a = $x;
   } else {
       $a = $y;
   }
   
   // static while
   while (1) {
       $a = $x;
   }
   
   // static do..while
   do {
       $a = $x;
   } while ('b'. 'c');
   
   // constant for() : No increment
   for ($i = 0; $i < 10; ) {
       $a = $x;
   }
   
   // constant for() : No final check
   for ( $i = 0; ; ++$i) {
       $a = $x;
   }
   
   
   // static ternary
   $a = TRUE ? $x : $y;
   
   ?>
Connex PHP features
-------------------

  + `condition <https://php-dictionary.readthedocs.io/en/latest/dictionary/condition.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConstantConditions                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


