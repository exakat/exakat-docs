.. _complete-createforeachdefault:

.. _create-foreach-default:

Create Foreach Default
++++++++++++++++++++++

.. meta::
	:description:
		Create Foreach Default: This command adds DEFAULT link from the blind variables to the literal definitions, when they are available.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Create Foreach Default
	:twitter:description: Create Foreach Default: This command adds DEFAULT link from the blind variables to the literal definitions, when they are available
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Create Foreach Default
	:og:type: article
	:og:description: This command adds DEFAULT link from the blind variables to the literal definitions, when they are available
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Create Foreach Default.html
	:og:locale: en
This command adds DEFAULT link from the blind variables to the literal definitions, when they are available. This adds sources for `static <https://www.php.net/manual/en/language.oop5.static.php>`_ loops, which are based on hardcoded list of data. Dynamic loops are not affected.

.. code-block:: php
   
   <?php
   
   // $a may b e 1, 2 or 3
   foreach([1,2,3] as $a) {
       echo $a;
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateForeachDefault                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


