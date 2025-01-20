.. _interfaces-php:

.. _php-interfaces:

PHP Interfaces
++++++++++++++

.. meta::
	:description:
		PHP Interfaces: List of PHP interfaces being used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Interfaces
	:twitter:description: PHP Interfaces: List of PHP interfaces being used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Interfaces
	:og:type: article
	:og:description: List of PHP interfaces being used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP Interfaces.html
	:og:locale: en
List of PHP interfaces being used in the code.

.. code-block:: php
   
   <?php
   
   // Countable is a PHP native interface
   class Enumeration extends Countable {
       function count() { return 1; }
   }
   
   ?>
Connex PHP features
-------------------

  + `interfaces <https://php-dictionary.readthedocs.io/en/latest/dictionary/interfaces.ini.html>`_
  + `native-php <https://php-dictionary.readthedocs.io/en/latest/dictionary/native-php.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/Php                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
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


