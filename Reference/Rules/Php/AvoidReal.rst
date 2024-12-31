.. _php-avoidreal:

.. _avoid-real:

Avoid Real
++++++++++

.. meta\:\:
	:description:
		Avoid Real: PHP has two float data type : real and double.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Real
	:twitter:description: Avoid Real: PHP has two float data type : real and double
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Real
	:og:type: article
	:og:description: PHP has two float data type : real and double
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/AvoidReal.html
	:og:locale: en
  PHP has two float data type : real and double. ``real`` is rarely used, and might be deprecated in PHP 7.4.

To prepare code, avoid using is_real() and the ``(real)`` typecast.

.. code-block:: php
   
   <?php
   
   // safe way to check for float
   if (!is_float($a)) {
       $a = (float) $a;
   }
   
   // Avoid doing that
   if (!is_real($a)) {
       $a = (real) $a;
   }
   
   ?>

See also `PHP RFC: Deprecations for PHP 7.4 <https://wiki.php.net/rfc/deprecations_php_7_4>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/The+%28real%29+cast+is+deprecated%2C+use+%28float%29+instead.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/The+%28real%29+cast+has+been+removed%2C+use+%28float%29+instead.html>`_



Connex PHP features
-------------------

  + `real <https://php-dictionary.readthedocs.io/en/latest/dictionary/real.ini.html>`_


Suggestions
___________

* Replace is_real() by is_float()
* Replace (real) by (float)




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AvoidReal                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


