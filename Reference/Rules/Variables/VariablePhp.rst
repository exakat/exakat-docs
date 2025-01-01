.. _variables-variablephp:

.. _php-variables:

PHP Variables
+++++++++++++

.. meta::
	:description:
		PHP Variables: This is the list of PHP predefined variables that are used in the application.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Variables
	:twitter:description: PHP Variables: This is the list of PHP predefined variables that are used in the application
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Variables
	:og:type: article
	:og:description: This is the list of PHP predefined variables that are used in the application
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/VariablePhp.html
	:og:locale: en
This is the list of PHP predefined variables that are used in the application. 

The web variables (``$_GET``, ``$_COOKIE``, ``$_FILES``) are quite commonly used, though sometimes replaced by some special accessors. Others are rarely used. 

.. code-block:: php
   
   <?php
   
   // Reading an incoming email, with sanitation
   $email = filter_var($_GET['email'], FILTER_SANITIZE_EMAIL);
   
   ?>

See also `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_.

Connex PHP features
-------------------

  + `superglobal <https://php-dictionary.readthedocs.io/en/latest/dictionary/superglobal.ini.html>`_
  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariablePhp                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


