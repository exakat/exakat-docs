.. _exceptions-definedexceptions:

.. _defined-exceptions:

Defined Exceptions
++++++++++++++++++

.. meta::
	:description:
		Defined Exceptions: This is the list of defined exceptions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Defined Exceptions
	:twitter:description: Defined Exceptions: This is the list of defined exceptions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Defined Exceptions
	:og:type: article
	:og:description: This is the list of defined exceptions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/DefinedExceptions.html
	:og:locale: en
This is the list of defined exceptions. Those exceptions are custom to the code, and shall be thrown at one point or more in the code.

.. code-block:: php
   
   <?php
   
   class myException extends \Exception {}
   
   // A defined exception
   throw new myException();
   
   // not a defined exception : it is already defined. 
   throw new \RuntimeException();
   
   ?>

See also `Predefined Exceptions <https://www.php.net/manual/en/reserved.exceptions.php>`_ and `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_.

Connex PHP features
-------------------

  + `predefined-exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/predefined-exception.ini.html>`_
  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/DefinedExceptions                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


