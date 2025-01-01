.. _functions-dynamiccall:

.. _dynamic-function-call:

Dynamic Function Call
+++++++++++++++++++++

.. meta::
	:description:
		Dynamic Function Call: Mark a functioncall made with a variable name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Function Call
	:twitter:description: Dynamic Function Call: Mark a functioncall made with a variable name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Function Call
	:og:type: article
	:og:description: Mark a functioncall made with a variable name
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/Dynamiccall.html
	:og:locale: en
Mark a functioncall made with a variable name. This means the function is only known at execution time, since it depends on the content of the variable. 

.. code-block:: php
   
   <?php
   
   // function definition
   function foo() {}
   
   // function name is in a variable, as a string.
   $var = 'foo'; 
   
   // dynamic call of a function
   $var();
   
   call_user_func($var);
   
   ?>
Connex PHP features
-------------------

  + `dynamic-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/Dynamiccall                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


