.. _exceptions-couldusetry:


.. _could-use-try:

Could Use Try
+++++++++++++

.. meta::
	:description:
		Could Use Try: Some commands may raise exceptions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Try
	:twitter:description: Could Use Try: Some commands may raise exceptions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Try
	:og:type: article
	:og:description: Some commands may raise exceptions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Try.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/CouldUseTry.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/CouldUseTry.html","name":"Could Use Try","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Some commands may raise exceptions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Try.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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

  + `Try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try-catch.ini.html>`_
  + `Exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `ArithmeticError Error <https://php-dictionary.readthedocs.io/en/latest/dictionary/arithmeticerror.ini.html>`_
  + `DivisionByZeroError <https://php-dictionary.readthedocs.io/en/latest/dictionary/divisionbyzeroerror.ini.html>`_
  + `ImagickException <https://php-dictionary.readthedocs.io/en/latest/dictionary/imagickexception.ini.html>`_
  + `ImagickPixelException <https://php-dictionary.readthedocs.io/en/latest/dictionary/imagickpixelexception.ini.html>`_
  + `InvalidArgumentException <https://php-dictionary.readthedocs.io/en/latest/dictionary/invalidargumentexception.ini.html>`_
  + `JsonException <https://php-dictionary.readthedocs.io/en/latest/dictionary/jsonexception.ini.html>`_
  + `mysqli_sql_exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/mysqli_sql_exception.ini.html>`_
  + `PDOException <https://php-dictionary.readthedocs.io/en/latest/dictionary/pdoexception.ini.html>`_
  + `PharException <https://php-dictionary.readthedocs.io/en/latest/dictionary/pharexception.ini.html>`_
  + `ReflectionException <https://php-dictionary.readthedocs.io/en/latest/dictionary/reflectionexception.ini.html>`_
  + `SVMException <https://php-dictionary.readthedocs.io/en/latest/dictionary/svmexception.ini.html>`_
  + `Type Error <https://php-dictionary.readthedocs.io/en/latest/dictionary/typerror.ini.html>`_
  + `UnexpectedValueException <https://php-dictionary.readthedocs.io/en/latest/dictionary/unexpectedvalueexception.ini.html>`_


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


