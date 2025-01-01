.. _structures-globaloutsideloop:

.. _global-inside-loop:

Global Inside Loop
++++++++++++++++++

.. meta::
	:description:
		Global Inside Loop: The global and static keywords must be used outside loops.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Global Inside Loop
	:twitter:description: Global Inside Loop: The global and static keywords must be used outside loops
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Global Inside Loop
	:og:type: article
	:og:description: The global and static keywords must be used outside loops
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/GlobalOutsideLoop.html
	:og:locale: en
The global and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ keywords must be used outside loops. Otherwise, they are evaluated at each loop, slowing the whole process.
This is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   // Here, global is used once
   global $total;
   foreach($a as $b) {
       $total += $b;
   }
   
   // Global is called each time : this is slow.
   foreach($a as $b) {
       global $total;
       $total += $b;
   }
   ?>

Suggestions
___________

* Move the global keyword outside the loop




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/GlobalOutsideLoop                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


