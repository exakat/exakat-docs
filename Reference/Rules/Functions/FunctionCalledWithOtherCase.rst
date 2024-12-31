.. _functions-functioncalledwithothercase:

.. _function-called-with-other-case-than-defined:

Function Called With Other Case Than Defined
++++++++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Function Called With Other Case Than Defined: Functions and methods are defined with a specific case.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Function Called With Other Case Than Defined
	:twitter:description: Function Called With Other Case Than Defined: Functions and methods are defined with a specific case
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Function Called With Other Case Than Defined
	:og:type: article
	:og:description: Functions and methods are defined with a specific case
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/FunctionCalledWithOtherCase.html
	:og:locale: en
  Functions and methods are defined with a specific case. Often, this is done on purpose,
either to distinguish the method from others, such as PHP natives functions, or to follow a naming
convention. 

PHP functions are case insensitive, which leads to situations like : 
It is recommended to use the same casing in the function call and the function definition.

.. code-block:: php
   
   <?php
     function myUtility($arg) { 
       /* some code here */
     } 
   
      myutility($var);
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_


Suggestions
___________

* Use the same case for the function and its call.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/FunctionCalledWithOtherCase                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


