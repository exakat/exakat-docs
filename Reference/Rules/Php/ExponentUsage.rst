.. _php-exponentusage:

.. _exponent-usage:

Exponent Usage
++++++++++++++

.. meta::
	:description:
		Exponent Usage: Usage of the ** operator or **=, to make exponents.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Exponent Usage
	:twitter:description: Exponent Usage: Usage of the ** operator or **=, to make exponents
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Exponent Usage
	:og:type: article
	:og:description: Usage of the ** operator or **=, to make exponents
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exponent Usage.html
	:og:locale: en
Usage of the `** <https://www.php.net/manual/en/language.operators.arithmetic.php>`_ operator or \*\*\=, to make exponents.

.. code-block:: php
   
   <?php
   
   $eight = 2 ** 3;
   
   $sixteen = 4;
   $sixteen \*\*\= 2;
   
   ?>

See also `Arithmetic Operators <https://www.php.net/manual/en/language.operators.arithmetic.php>`_.

Connex PHP features
-------------------

  + `exponent <https://php-dictionary.readthedocs.io/en/latest/dictionary/exponent.ini.html>`_


Suggestions
___________

* Use the operator when no literal negative number is in the expression




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ExponentUsage                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and more recent                                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


