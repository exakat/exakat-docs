.. _constants-constantusage:

.. _constants-usage:

Constants Usage
+++++++++++++++

.. meta::
	:description:
		Constants Usage: List of constants in use in the source code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constants Usage
	:twitter:description: Constants Usage: List of constants in use in the source code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constants Usage
	:og:type: article
	:og:description: List of constants in use in the source code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Constants/ConstantUsage.html
	:og:locale: en
List of constants in use in the source code. Constants are `T_STRING <https://www.php.net/T_STRING>`_, localised in specific part of the code. 

For example, they can't be followed by a parenthesis, as this is a function call; nor preceded by a ``new`` operator, as this is an object instantiation. 

.. code-block:: php
   
   <?php
   
   const MY_CONST = 'Hello';
   
   // PHP_EOL (native PHP Constant)
   // MY_CONST (custom constant)
   echo PHP_EOL . MY_CONST;
   
   // Here, MY_CONST is actually a function name, and is omitted in this analysis
   MY_CONST();
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConstantUsage                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


