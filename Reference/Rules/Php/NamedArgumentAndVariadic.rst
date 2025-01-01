.. _php-namedargumentandvariadic:

.. _named-argument-and-variadic:

Named Argument And Variadic
+++++++++++++++++++++++++++

.. meta::
	:description:
		Named Argument And Variadic: Variadic argument must be the last in the list of arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Named Argument And Variadic
	:twitter:description: Named Argument And Variadic: Variadic argument must be the last in the list of arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Named Argument And Variadic
	:og:type: article
	:og:description: Variadic argument must be the last in the list of arguments
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/NamedArgumentAndVariadic.html
	:og:locale: en
Variadic argument must be the last in the list of arguments. Since PHP 8.1, it is possible to use named arguments after a variadic argument.

.. code-block:: php
   
   <?php
     // named arguments may be after the variadic
     foo(...$a, a: 1);
     
     // positional arguments MUST be before the variadic
     foo(...$a,  1);
     
     // Normal way
     foo( 1, ...$a);
   ?>
Related PHP errors 
-------------------

  + `Cannot combine named arguments and argument unpacking <https://php-errors.readthedocs.io/en/latest/messages/cannot-combine-named-arguments-and-argument-unpacking.html>`_
  + `Cannot use positional argument after argument unpacking <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-positional-argument-after-argument-unpacking.html>`_




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


