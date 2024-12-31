.. _php-autoloadusage:

.. _autoloading:

Autoloading
+++++++++++

.. meta\:\:
	:description:
		Autoloading: Usage of the autoloading feature of PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Autoloading
	:twitter:description: Autoloading: Usage of the autoloading feature of PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Autoloading
	:og:type: article
	:og:description: Usage of the autoloading feature of PHP
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/AutoloadUsage.html
	:og:locale: en
  Usage of the autoloading feature of PHP. 
Defining the __autoload() function is obsolete since PHP 7.2.

.. code-block:: php
   
   <?php
   
   spl_autoload_register('my_autoloader');
   
   // Old way to autoload. Deprecated in PHP 7.2
   function __autoload($class ) {}
   
   ?>

See also `__autoload <https://www.php.net/autoload>`_.

Connex PHP features
-------------------

  + `autoload <https://php-dictionary.readthedocs.io/en/latest/dictionary/autoload.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AutoloadUsage                                                                                                                                                                       |
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


