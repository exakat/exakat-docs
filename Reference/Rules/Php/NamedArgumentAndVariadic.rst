.. _php-namedargumentandvariadic:

.. _named-arguments-and-variadic:

Named Arguments And Variadic
++++++++++++++++++++++++++++

.. meta::
	:description:
		Named Arguments And Variadic: Variadic arguments must be the lasts in the list of arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Named Arguments And Variadic
	:twitter:description: Named Arguments And Variadic: Variadic arguments must be the lasts in the list of arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Named Arguments And Variadic
	:og:type: article
	:og:description: Variadic arguments must be the lasts in the list of arguments
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Named Arguments And Variadic.html
	:og:locale: en
Variadic arguments must be the lasts in the list of arguments. Since PHP 8.1, it is possible to use named arguments after a variadic argument.

.. code-block:: php
   
   <?php
      function foo($a, $b) {}
   
      $args = ['b' => 2];
   
     // named arguments may be after the variadic
     foo(...$args, a: 1);
     
     // Fatal error: positional arguments MUST be before the variadic
     foo(...$args,  1);
     
     // positional way of laying the arguments
     foo(1, ...$args);
   ?>
Related PHP errors 
-------------------

  + `Cannot combine named arguments and argument unpacking <https://php-errors.readthedocs.io/en/latest/messages/cannot-combine-named-arguments-and-argument-unpacking.html>`_
  + `Cannot use positional argument after argument unpacking <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-positional-argument-after-argument-unpacking.html>`_



Connex PHP features
-------------------

  + `variadic <https://php-dictionary.readthedocs.io/en/latest/dictionary/variadic.ini.html>`_
  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Always put the variadic at the end of the argument list




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NamedArgumentAndVariadic                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


