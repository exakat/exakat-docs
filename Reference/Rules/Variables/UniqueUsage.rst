.. _variables-uniqueusage:

.. _single-use-variables:

Single Use Variables
++++++++++++++++++++

.. meta::
	:description:
		Single Use Variables: This is the list of variables that are written, then read, and only used once.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Single Use Variables
	:twitter:description: Single Use Variables: This is the list of variables that are written, then read, and only used once
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Single Use Variables
	:og:type: article
	:og:description: This is the list of variables that are written, then read, and only used once
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Single Use Variables.html
	:og:locale: en
This is the list of variables that are written, then read, and only used once.

Single-use variables may be trimmed down, and the initial expression may be used instead.

Single-use variables may improve readability, when the final expression grows too much with the extra expression. 


.. code-block:: php
   
   <?php
   
   function foo($d) {
       $a = 1;     // $a is used twice
       $b = $a + 2;  // $b is used once
       $c = $a + $b + $d; // $c is also used once
       // $d is an argument, so it's OK.
       
       retrun $c;
   }
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Merge the two expressions into one larger
* Make a second use of the variable
* Inline the code of the expression instead of the variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UniqueUsage                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                   |
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


