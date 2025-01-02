.. _php-ellipsisusage:

.. _ellipsis-usage:

Ellipsis Usage
++++++++++++++

.. meta::
	:description:
		Ellipsis Usage: Usage of the ellipsis keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ellipsis Usage
	:twitter:description: Ellipsis Usage: Usage of the ellipsis keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ellipsis Usage
	:og:type: article
	:og:description: Usage of the ellipsis keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Ellipsis Usage.html
	:og:locale: en
Usage of the ellipsis keyword. The keyword is three dots : ``...`` . It is also named variadic or splat operator.

It may be in function definitions and function calls; it may be in arrays; it is also usable with parenthesis.

`... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ allows for packing or unpacking arguments into an array.

.. code-block:: php
   
   <?php
   
   $args = [1, 2, 3];
   foo(...$args); 
   // Identical to foo(1,2,3);
   
   function bar(...$a) {
       // Identical to : $a = func_get_args();
   }
   ?>

See also `PHP RFC: Syntax for variadic functions <https://wiki.php.net/rfc/variadics>`_, `PHP 5.6 and the Splat Operator <https://lornajane.net/posts/2014/php-5-6-and-the-splat-operator>`_ and `Variable-length argument lists <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_.

Connex PHP features
-------------------

  + `ellipsis <https://php-dictionary.readthedocs.io/en/latest/dictionary/ellipsis.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/EllipsisUsage                                                                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and more recent                                                                                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


