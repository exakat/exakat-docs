.. _php-incomingvariables:

.. _incoming-variables:

Incoming Variables
++++++++++++++++++

.. meta::
	:description:
		Incoming Variables: Incoming names, used across the application.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incoming Variables
	:twitter:description: Incoming Variables: Incoming names, used across the application
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incoming Variables
	:og:type: article
	:og:description: Incoming names, used across the application
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incoming Variables.html
	:og:locale: en
Incoming names, used across the application. 

Incoming variables are first-level index in ``$_POST``, ``$_GET``, ``$_COOKIE``, ``$_REQUEST`` and ``$_FILE``;

``$_SESSION`` and ``$_ENV`` are not reported as incoming data, as they are not supposed to be manipulated by normal user. 

Dynamic names are not reported too.

.. code-block:: php
   
   <?php
   
   $name = $_GET['name'];
   $cookie = $_COOKIE['cookie'];
   
   // 'archive' is the incoming variable, not 'file_name'
   $file_name = $_FILE['archive']['file_name'];
   
   // This is not reported, because it is from $_ENV.
   $db_pass = $_ENV['DB_PASS'];
   
   // This is not reported, because it is dynamic
   $x = 'userId';
   $userId = $_GET[$x];
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IncomingVariables                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Inventory <ruleset-Inventory>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


