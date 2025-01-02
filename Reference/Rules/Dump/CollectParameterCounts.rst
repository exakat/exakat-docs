.. _dump-collectparametercounts:

.. _collect-parameter-counts:

Collect Parameter Counts
++++++++++++++++++++++++

.. meta::
	:description:
		Collect Parameter Counts: This analysis collects the number of parameter per method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Parameter Counts
	:twitter:description: Collect Parameter Counts: This analysis collects the number of parameter per method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Parameter Counts
	:og:type: article
	:og:description: This analysis collects the number of parameter per method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Parameter Counts.html
	:og:locale: en
This analysis collects the number of parameter per method. 

The count applies to functions, methods, closures and arrow functions.

.. code-block:: php
   
   <?php
   
   // parameter count on function : 1
   function foo($a) { }
   
   // parameter count on closure : 2
   function ($b, $c = 2) {}
   
   // parameter count on method : 0 (none)
   class x {
       function moo() { }
   }
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectParameterCounts                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


