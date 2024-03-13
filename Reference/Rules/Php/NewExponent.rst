.. _php-newexponent:

.. _**-for-exponent:

** For Exponent
+++++++++++++++

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
| Features     | exponential                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-traq-php-newexponent`, :ref:`case-teampass-php-newexponent`                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


