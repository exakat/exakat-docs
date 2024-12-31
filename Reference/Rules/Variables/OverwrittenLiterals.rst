.. _variables-overwrittenliterals:

.. _overwritten-literals:

Overwritten Literals
++++++++++++++++++++

.. meta\:\:
	:description:
		Overwritten Literals: The same variable is assigned a literal twice.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Literals
	:twitter:description: Overwritten Literals: The same variable is assigned a literal twice
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Literals
	:og:type: article
	:og:description: The same variable is assigned a literal twice
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/OverwrittenLiterals.html
	:og:locale: en
  The same variable is assigned a literal twice. It is possible that one of the assignation is too many.

This analysis doesn't take into account the distance between two assignations : it may report false positives when the variable is actually used for several purposes, and, as such, assigned twice with different values.

.. code-block:: php
   
   <?php
   
   function foo() {
       // Two assignations in a short sequence : one is too many.
       $a = 1;
       $a = 2;
       
       for($i = 0; $i < 10; $i++) {
           $a += $i;
       }
       $b = $a;
       
       // New assignation. $a is now used as an array. 
       $a = array(0);
   }
   
   ?>
Connex PHP features
-------------------

  + `literal <https://php-dictionary.readthedocs.io/en/latest/dictionary/literal.ini.html>`_


Suggestions
___________

* Remove one of the assignation (the earliest)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/OverwrittenLiterals                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


