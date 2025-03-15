.. _structures-variadicandfuncgetarg:


.. _variadic-and-func\_get\_arg():

Variadic And func_get_arg()
+++++++++++++++++++++++++++

.. meta::
	:description:
		Variadic And func_get_arg(): Using a variadic parameter in the method signature removes the final parameters of a function call from the result of func_get_args().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variadic And func_get_arg()
	:twitter:description: Variadic And func_get_arg(): Using a variadic parameter in the method signature removes the final parameters of a function call from the result of func_get_args()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variadic And func_get_arg()
	:og:type: article
	:og:description: Using a variadic parameter in the method signature removes the final parameters of a function call from the result of func_get_args()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variadic And func_get_arg().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/VariadicAndFuncGetArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/VariadicAndFuncGetArg.html","name":"Variadic And func_get_arg()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Using a variadic parameter in the method signature removes the final parameters of a function call from the result of func_get_args()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Variadic And func_get_arg().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Using a variadic parameter in the method signature removes the final parameters of a function call from the `result <https://www.php.net/result>`_ of `func_get_args() <https://www.php.net/func_get_args>`_. 

This behavior is not the case when the variadic is not present. It is recommended to check if that parameter is not forgotten in the processing of the method.

.. code-block:: php
   
   <?php
   
   function foo($a, ...$b) {
       print_r(func_get_args());
       // array( 1 )
   }
   foo(1,2,3);
   
   function goo($a, $b) {
       print_r(func_get_args());
       // array( 1, 2, 3)
   }
   foo(1,2,3);
   
   
   ?>
Connex PHP features
-------------------

  + `Variadic <https://php-dictionary.readthedocs.io/en/latest/dictionary/variadic.ini.html>`_
  + `func_get_args <https://php-dictionary.readthedocs.io/en/latest/dictionary/func_get_args.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/VariadicAndFuncGetArg                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Unknown                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


