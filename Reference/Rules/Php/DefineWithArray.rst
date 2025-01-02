.. _php-definewitharray:

.. _define-constants-with-array:

Define Constants With Array
+++++++++++++++++++++++++++

.. meta::
	:description:
		Define Constants With Array: PHP has the ability to define an array as a constant, using the define() native call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Define Constants With Array
	:twitter:description: Define Constants With Array: PHP has the ability to define an array as a constant, using the define() native call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Define Constants With Array
	:og:type: article
	:og:description: PHP has the ability to define an array as a constant, using the define() native call
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Define Constants With Array.html
	:og:locale: en
PHP has the ability to define an array as a constant, using the `define() <https://www.php.net/define>`_ native call. This was not possible until that version, only with the const keyword.

This was introduced in PHP 7.0. It also applies to the ``const`` keyword and to class constants.


.. code-block:: php
   
   <?php
   
   //Defining an array as a constant
   define('MY_PRIMES', [2, 3, 5, 7, 11]);
   
   const MY_OTHER_NUMBERS =  [12, 13, 15, 17, 111];
   
   ?>
Connex PHP features
-------------------

  + `define <https://php-dictionary.readthedocs.io/en/latest/dictionary/define.ini.html>`_
  + `const <https://php-dictionary.readthedocs.io/en/latest/dictionary/const.ini.html>`_
  + `static-constant-expression <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-constant-expression.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DefineWithArray                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


