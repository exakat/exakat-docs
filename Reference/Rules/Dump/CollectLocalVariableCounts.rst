.. _dump-collectlocalvariablecounts:

.. _collect-local-variable-counts:

Collect Local Variable Counts
+++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Collect Local Variable Counts: This analysis collects the number of local variables used in a method or a function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Local Variable Counts
	:twitter:description: Collect Local Variable Counts: This analysis collects the number of local variables used in a method or a function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Local Variable Counts
	:og:type: article
	:og:description: This analysis collects the number of local variables used in a method or a function
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectLocalVariableCounts.html
	:og:locale: en
  This analysis collects the number of local variables used in a method or a function. 

The count applies to functions, methods, closures and arrow functions. 

Arguments and global variables are not counted. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are.

.. code-block:: php
   
   <?php
   
   function foo($arg) {
       global $w;
       
       // This is a local variable
       $x = rand(1, 2);
       
       return $x + $arg + $w;
   }
   
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectLocalVariableCounts                                                                                                                                                         |
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


