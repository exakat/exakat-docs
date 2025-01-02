.. _php-php80namedparametervariadic:

.. _php-80-named-parameter-variadic:

PHP 80 Named Parameter Variadic
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		PHP 80 Named Parameter Variadic: Named parameter with variadic have been renamed from 0 to 'parameter name' in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 80 Named Parameter Variadic
	:twitter:description: PHP 80 Named Parameter Variadic: Named parameter with variadic have been renamed from 0 to 'parameter name' in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 80 Named Parameter Variadic
	:og:type: article
	:og:description: Named parameter with variadic have been renamed from 0 to 'parameter name' in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 80 Named Parameter Variadic.html
	:og:locale: en
Named parameter with variadic have been renamed from 0 to 'parameter name' in PHP 8.0.
In PHP 7.0, with positional argument only, the content of $b is in an array, index 0. This is also true with PHP 8.0.

In PHP 8.0, with named arguments, the content of $b is in an array, index 'b';

Since the behavior of the variadic depends on the calling syntax (with or without named parameter), the receiving must ensure the correct reception, and handle both cases.

.. code-block:: php
   
   <?php
   
   function foo($a, ...$b) {
       print_r($b);
   }
   
   foo(3, 4);
   foo(3, b: 4);              // PHP 8 only 
   foo(...[2, "b"=> [3, 4]]); // PHP 8 only 
   
   ?>
Connex PHP features
-------------------

  + `variadic <https://php-dictionary.readthedocs.io/en/latest/dictionary/variadic.ini.html>`_
  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Apply array_values() to the variadic arguments.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/Php80NamedParameterVariadic                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.0                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and more recent                                                                                                                                                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0+                                                                                                                                                                                |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Medium                                                                                                                                                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


