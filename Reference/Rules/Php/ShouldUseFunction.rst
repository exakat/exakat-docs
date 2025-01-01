.. _php-shouldusefunction:

.. _should-use-function:

Should Use Function
+++++++++++++++++++

.. meta::
	:description:
		Should Use Function: Functioncalls that fall back to global scope should be using 'use function' or be fully namespaced.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Function
	:twitter:description: Should Use Function: Functioncalls that fall back to global scope should be using 'use function' or be fully namespaced
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Function
	:og:type: article
	:og:description: Functioncalls that fall back to global scope should be using 'use function' or be fully namespaced
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ShouldUseFunction.html
	:og:locale: en
Functioncalls that fall back to global scope should be using 'use function' or be fully namespaced. 

PHP searches for functions in the local namespaces, and in case it fails, makes the same search in the global scope. Anytime a native function is referenced this way, the search (and fail) happens. This slows down the scripts.

The speed bump range from 2 to 8 %, depending on the availability of functions in the local scope. The overall bump is about 1 µs per functioncall, which makes it a micro optimisation until a lot of function calls are made.

Based on one of `Marco Pivetta tweet <https://twitter.com/Ocramius/status/811504929357660160>`_.
This analysis is a related to Performances/Php74ArrayKeyExists, and is a more general version.

.. code-block:: php
   
   <?php
   
   namespace X {
       use function strtolower as strtolower_aliased;
       
       // PHP searches for strtolower in X, fails, then falls back to global scope, succeeds.
       $a = strtolower($b);
   
       // PHP searches for strtolower in global scope, succeeds.
       $a = \strtolower($b);
   
       // PHP searches for strtolower_aliased in global scope, succeeds.
       $a = \strtolower_aliased($b);
   }
   
   ?>

See also `blog post <http://veewee.github.io/blog/optimizing-php-performance-by-fq-function-calls/>`_.


Suggestions
___________

* Use the `use` command for arrray_key_exists(), at the beginning of the script
* Use an initial \ before array_key_exists()
* Remove the namespace




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShouldUseFunction                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.5                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


