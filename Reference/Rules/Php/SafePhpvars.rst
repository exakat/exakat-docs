.. _php-safephpvars:

.. _safe-phpvariables:

Safe Phpvariables
+++++++++++++++++

.. meta\:\:
	:description:
		Safe Phpvariables: Mark the safe PHP variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Safe Phpvariables
	:twitter:description: Safe Phpvariables: Mark the safe PHP variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Safe Phpvariables
	:og:type: article
	:og:description: Mark the safe PHP variables
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/SafePhpvars.html
	:og:locale: en
  Mark the safe PHP variables. 

PHP superglobals are usually filled with external data that should be filtered. However, some values may be considered safe, as they are under the control of the developer.

``$_GET``, ``$_POST``, ``$_FILES``, ``$_REQUEST``, ``$_COOKIES`` are all considered unsafe. Their level of validation is checked in other analysis. 

``$_SERVER`` is partially safe. It is valid for the following values : ``DOCUMENT_ROOT``, ``REQUEST_TIME``, ``REQUEST_TIME_FLOAT``, ``SCRIPT_NAME``, ``SERVER_ADMIN``, ``_``.

.. code-block:: php
   
   <?php
   
   // DOCUMENT_ROOT is a safe variable
   echo $_SERVER['DOCUMENT_ROOT'];
   
   // $_SERVER's PHP_SELF MUST be validated before usage
   echo $_SERVER['PHP_SELF'];
   
   // $_GET MUST be validated before usage
   echo $_GET['_'];
   
   ?>

See also `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_.

Connex PHP features
-------------------

  + `superglobal <https://php-dictionary.readthedocs.io/en/latest/dictionary/superglobal.ini.html>`_
  + `php-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/php-variable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SafePhpvars                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


