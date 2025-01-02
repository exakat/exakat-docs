.. _dump-argumentcountspercalls:

.. _argument-counts-per-calls:

Argument Counts Per Calls
+++++++++++++++++++++++++

.. meta::
	:description:
		Argument Counts Per Calls: Collects the number of arguments passed to PHP functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Argument Counts Per Calls
	:twitter:description: Argument Counts Per Calls: Collects the number of arguments passed to PHP functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Argument Counts Per Calls
	:og:type: article
	:og:description: Collects the number of arguments passed to PHP functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Argument Counts Per Calls.html
	:og:locale: en
Collects the number of arguments passed to PHP functions. 

This is focused on PHP native functions, with optional characters.
This helps detect unused or lesser know arguments.

.. code-block:: php
   
   <?php
   
   // One entry, in_array 2 arguments
   $c = in_array($array, $needle);
   
   // One entry, in_array 3 arguments
   $c = in_array($array, $needle, true);
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/ArgumentCountsPerCalls                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
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


