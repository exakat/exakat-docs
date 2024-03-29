.. _extensions-extdecimal:

.. _ext-decimal:

ext/decimal
+++++++++++

  Extension php-decimal, by ``Rudi Theunissen``.

This library provides a PHP extension that adds support for correctly-rounded, arbitrary-precision decimal floating point arithmetic. Applications that rely on accurate numbers (ie. money, measurements, or mathematics) can use Decimal instead of float or string to represent numerical values.

.. code-block:: php
   
   <?php
   
   use Decimal\Decimal;
   
   $op1 = new Decimal("0.1", 4);
   $op2 = "0.123456789";
   
   print_r($op1 + $op2);
   
   
   use Decimal\Decimal;
   
   /**
    * @param int $n The factorial to calculate, ie. $n!
    * @param int $p The precision to calculate the factorial to.
    *
    * @return Decimal
    */
   function factorial(int $n, int $p = Decimal::DEFAULT_PRECISION): Decimal
   {
       return $n < 2 ? new Decimal($n, $p) : $n * factorial($n - 1, $p);
   }
   
   echo factorial(10000, 32);
   
   ?>

See also `PHP Decimal <http://php-decimal.io>`_ and `libmpdec <http://www.bytereef.org/mpdecimal/quickstart.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extdecimal                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | extension, float                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


