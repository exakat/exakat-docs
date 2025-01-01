.. _php-newexponent:

.. _**-for-exponent:

** For Exponent
+++++++++++++++

.. meta::
	:description:
		** For Exponent: The operator ``**`` calculates exponents, also known as power.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ** For Exponent
	:twitter:description: ** For Exponent: The operator ``**`` calculates exponents, also known as power
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ** For Exponent
	:og:type: article
	:og:description: The operator ``**`` calculates exponents, also known as power
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/NewExponent.html
	:og:locale: en
The operator ``**`` calculates exponents, also known as power. 

Use it instead of the slower function `pow() <https://www.php.net/pow>`_. This operator was introduced in PHP 5.6.
Be aware the the '-' operator has lower priority than the `** <https://www.php.net/manual/en/language.operators.arithmetic.php>`_ operator : this leads to the following confusing `result <https://www.php.net/result>`_.
This is due to the parser that processes separately ``-`` and the following number. Since ``**`` has priority, the power operation happens first.

Being an operator, ``**`` is faster than `pow() <https://www.php.net/pow>`_. This is a microoptimisation.

.. code-block:: php
   
   <?php
       $cube = pow(2, 3); // 8
   
       $cubeInPHP56 = 2 ** 3; // 8
   ?>

See also `Arithmetic Operators <https://www.php.net/manual/en/language.operators.arithmetic.php>`_.

Connex PHP features
-------------------

  + `exponential <https://php-dictionary.readthedocs.io/en/latest/dictionary/exponential.ini.html>`_


Suggestions
___________

* Use the ``**`` operator
* For powers of 2, use the bitshift operators
* For literal powers of 2, consider using the ``0xFFFFFFFFF`` syntax.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NewExponent                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and more recent                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-traq-php-newexponent`, :ref:`case-teampass-php-newexponent`                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


