.. _functions-usearrowfunctions:

.. _use-arrow-functions:

Use Arrow Functions
+++++++++++++++++++

.. meta::
	:description:
		Use Arrow Functions: Arrow functions are closures that require one expression of code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Arrow Functions
	:twitter:description: Use Arrow Functions: Arrow functions are closures that require one expression of code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Arrow Functions
	:og:type: article
	:og:description: Arrow functions are closures that require one expression of code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UseArrowFunctions.html
	:og:locale: en
Arrow functions are closures that require one expression of code. They also include all the variables of the current context, unless they are made `static <https://www.php.net/manual/en/language.oop5.static.php>`_.

Arrow functions were introduced in PHP 7.4. They added the reserved keyword ``fn``.

.. code-block:: php
   
   <?php
   
   array_map(fn(A $b): int => $b->c, $array);
   
   function array_values_from_keys($arr, $keys) {
       return array_map(fn($x) => $arr[$x], $keys);
   }
   ?>

See also `RFC : Arrow functions <https://wiki.php.net/rfc/arrow_functions>`_ and `Arrow functions in PHP <https://stitcher.io/blog/short-closures-in-php>`_.

Connex PHP features
-------------------

  + `arrow-function <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrow-function.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UseArrowFunctions                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`One Liners <ruleset-One-Liners>`          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


