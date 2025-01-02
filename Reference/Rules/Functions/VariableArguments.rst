.. _functions-variablearguments:

.. _has-variable-arguments:

Has Variable Arguments
++++++++++++++++++++++

.. meta::
	:description:
		Has Variable Arguments: Indicates if this function or method accept an arbitrary number of arguments, based on func_get_args(), func_get_arg() and func_num_args() usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Has Variable Arguments
	:twitter:description: Has Variable Arguments: Indicates if this function or method accept an arbitrary number of arguments, based on func_get_args(), func_get_arg() and func_num_args() usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Has Variable Arguments
	:og:type: article
	:og:description: Indicates if this function or method accept an arbitrary number of arguments, based on func_get_args(), func_get_arg() and func_num_args() usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Has Variable Arguments.html
	:og:locale: en
Indicates if this function or method accept an arbitrary number of arguments, based on `func_get_args() <https://www.php.net/func_get_args>`_, `func_get_arg() <https://www.php.net/func_get_arg>`_ and `func_num_args() <https://www.php.net/func_num_args>`_ usage.

.. code-block:: php
   
   <?php
   
   // Fixed number of arguments
   function fixedNumberOfArguments($a, $b) {
       if (func_num_args() > 2) {
           $c = func_get_args();
           array_shift($c); // $a
           array_shift($c); // $b
       }
       // do something
   }
   
   // Fixed number of arguments
   function fixedNumberOfArguments($a, $b, $c = 1) {}
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/VariableArguments                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


