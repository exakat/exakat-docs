.. _functions-uselessdefault:

.. _useless-default-argument:

Useless Default Argument
++++++++++++++++++++++++

.. meta::
	:description:
		Useless Default Argument: One of the argument has a default value, and this default value is never used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Default Argument
	:twitter:description: Useless Default Argument: One of the argument has a default value, and this default value is never used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Default Argument
	:og:type: article
	:og:description: One of the argument has a default value, and this default value is never used
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UselessDefault.html
	:og:locale: en
One of the argument has a default value, and this default value is never used. Every time the method is called, the argument is provided explicitly, rendering the default value actually useless.

.. code-block:: php
   
   <?php
   
   function goo($a, $b = 3) { 
       // do something here
   }
   
   // foo is called 3 times, and sometimes, $b is not provided. 
   goo(1,2);
   goo(1,2);
   goo(1);
   
   
   function foo($a, $b = 3) { 
       // do something here
   }
   
   // foo is called 3 times, and $b is always provided. 
   foo(1,2);
   foo(1,2);
   foo(1,2);
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `default <https://php-dictionary.readthedocs.io/en/latest/dictionary/default.ini.html>`_


Suggestions
___________

* Remove the default value
* Remove the explicit argument in the function call, when it is equal to the default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessDefault                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                   |
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


