.. _performances-autoappend:

.. _autoappend:

Autoappend
++++++++++

.. meta::
	:description:
		Autoappend: Appending a variable to itself leads to enormous usage of memory.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Autoappend
	:twitter:description: Autoappend: Appending a variable to itself leads to enormous usage of memory
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Autoappend
	:og:type: article
	:og:description: Appending a variable to itself leads to enormous usage of memory
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Autoappend.html
	:og:locale: en
Appending a variable to itself leads to enormous usage of memory.

.. code-block:: php
   
   <?php
   
   // Always append a value to a distinct variable
   foreach($a as $b) {
       $c[] = $b;
   }
   
   // This copies the array to itself, and double the size each loop
   foreach($a as $b) {
       $c[] = $c;
   }
   ?>

Suggestions
___________

* Change the variable on the left of the append
* Change the variable on the right of the append




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/Autoappend                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                    |
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


