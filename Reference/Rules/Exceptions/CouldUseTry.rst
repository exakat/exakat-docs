.. _exceptions-couldusetry:

.. _could-use-try:

Could Use Try
+++++++++++++

  Some commands may raise exceptions. It is recommended to use the try/catch block to intercept those exceptions, and process them.

* / : ``DivisionByZeroError``
* % : ``DivisionByZeroError``
* `intdiv() <https://www.php.net/intdiv>`_ : ``DivisionByZeroError``, ``ArithmeticError``
* << : ``ArithmeticError``
* >> : ``ArithmeticError``
* ``Phar\:\:mungserver`` : ``PharException``
* ``Phar\:\:webphar`` : ``PharException``

Some exceptions have an extra analysis, due to special detection condition : ``ParseError``, with eval() and ``DivisionByZeroError``.



.. code-block:: php
   
   <?php
   
   function division(int $a, int $b) {
   	// This expression might generate a DivisionByZeroError, and require a try/catch for error handling purposes.
   	return $a / $b;
   }
   
   ?>

See also `Predefined Exceptions <https://www.php.net/manual/en/reserved.exceptions.php>`_ and `PharException <https://www.php.net/manual/en/class.pharexception.php>`_.

Connex PHP features
-------------------

  + `try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try-catch.ini.html>`_
  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `arithmeticerror <https://php-dictionary.readthedocs.io/en/latest/dictionary/arithmeticerror.ini.html>`_
  + `divisionbyzeroerror <https://php-dictionary.readthedocs.io/en/latest/dictionary/divisionbyzeroerror.ini.html>`_
  + `imagickexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/imagickexception.ini.html>`_
  + `imagickpixelexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/imagickpixelexception.ini.html>`_
  + `invalidargumentexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/invalidargumentexception.ini.html>`_
  + `jsonexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/jsonexception.ini.html>`_
  + `mysqli_sql_exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/mysqli_sql_exception.ini.html>`_
  + `pdoexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/pdoexception.ini.html>`_
  + `pharexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/pharexception.ini.html>`_
  + `reflectionexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/reflectionexception.ini.html>`_
  + `svmexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/svmexception.ini.html>`_
  + `typerror <https://php-dictionary.readthedocs.io/en/latest/dictionary/typerror.ini.html>`_
  + `unexpectedvalueexception <https://php-dictionary.readthedocs.io/en/latest/dictionary/unexpectedvalueexception.ini.html>`_


Suggestions
___________

* Add a try/catch clause around those commands
* Add a check on the values used with those operator : for example, check a dividend is not 0, or a bitshift is not negative




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CouldUseTry                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mautic-exceptions-couldusetry`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`eval()-without-try`, :ref:`check-division-by-zero`                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


