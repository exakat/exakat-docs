.. _performances-php7encapsedstrings:

.. _use-php7-encapsed-strings:

Use PHP7 Encapsed Strings
+++++++++++++++++++++++++

.. meta::
	:description:
		Use PHP7 Encapsed Strings: PHP 7 has optimized the handling of double-quoted strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use PHP7 Encapsed Strings
	:twitter:description: Use PHP7 Encapsed Strings: PHP 7 has optimized the handling of double-quoted strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use PHP7 Encapsed Strings
	:og:type: article
	:og:description: PHP 7 has optimized the handling of double-quoted strings
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Performances/PHP7EncapsedStrings.html
	:og:locale: en
PHP 7 has optimized the handling of double-quoted strings. In particular, double-quoted strings are much less memory hungry than classic concatenations. 

PHP allocates memory at the end of the double-quoted string, making only one call to the allocator. On the other hand, concatenations are allocated each time they include dynamic content, leading to higher memory consumption. 
Concatenations are still needed with constants, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ constants, magic constants, functions, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods.

.. code-block:: php
   
   <?php
   
   $bar = 'bar';
    
   /* PHP 7 optimized this */
   $a = "foo and $bar";
   
   /* This is PHP 5 code (aka, don't use it) */
   $a = 'foo and ' . $bar;
   
   // Constants can't be used with double quotes
   $a = 'foo and ' . __DIR__;
   $a = "foo and __DIR__"; // __DIR__ is not interpolated
   
   ?>

See also `PHP 7 performance improvements (3/5): Encapsed strings optimization <https://blog.blackfire.io/php-7-performance-improvements-encapsed-strings-optimization.html>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/PHP7EncapsedStrings                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


