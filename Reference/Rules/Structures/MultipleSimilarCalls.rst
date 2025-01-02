.. _structures-multiplesimilarcalls:

.. _multiple-similar-calls:

Multiple Similar Calls
++++++++++++++++++++++

.. meta::
	:description:
		Multiple Similar Calls: Several calls are made to functions or methods in a row.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Similar Calls
	:twitter:description: Multiple Similar Calls: Several calls are made to functions or methods in a row
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Similar Calls
	:og:type: article
	:og:description: Several calls are made to functions or methods in a row
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Similar Calls.html
	:og:locale: en
Several calls are made to functions or methods in a row. They may have different arguments, though having a lot of similar calls in a row may indicate that a loop is needed. 



Alternatively, some native PHP functions use an arbitrary number of arguments to avoid multiple calls to the same function. For example, it is possible to call `array_merge() <https://www.php.net/array_merge>`_ once, or a loop on `.=` may be replaced with a call to `implode() <https://www.php.net/implode>`_.

.. code-block:: php
   
   <?php
   
   echo $a[1];
   echo $a[2];
   echo $a[3];
   echo $a[4];
   echo $a[5];
   
   // This could be 
   foreach($a as $v) {
       echo $v;
   }
   
   if (isset($a) && isset($b) && isset($c) && isset($d)) { }
   
   // This could be coded as
   if (isset($a, $b, $c, $d)) { }
   
   ?>

Suggestions
___________

* Move the calls to a loop
* Tactically use one call to a function with multiple arguments. For example, isset() with multiple arguments.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleSimilarCalls                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


