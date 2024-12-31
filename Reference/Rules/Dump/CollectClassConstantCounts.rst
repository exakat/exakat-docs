.. _dump-collectclassconstantcounts:

.. _collect-class-constant-counts:

Collect Class Constant Counts
+++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Collect Class Constant Counts: This analysis collects the number of class constants per class or interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Class Constant Counts
	:twitter:description: Collect Class Constant Counts: This analysis collects the number of class constants per class or interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Class Constant Counts
	:og:type: article
	:og:description: This analysis collects the number of class constants per class or interface
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectClassConstantCounts.html
	:og:locale: en
  This analysis collects the number of class constants per class or interface. 

The count applies to classes, anonymous classes and interfaces. They are considered distinct one from another.

.. code-block:: php
   
   <?php
   
   class foo {
       // 3 constant
       const A =1, B =2;
   }
   
   interface bar {
       // 3 properties
       const A=1, B=2, C=3;
   }
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectClassConstantCounts                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
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


