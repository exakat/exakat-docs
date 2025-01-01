.. _constants-phpconstantusage:

.. _php-constant-usage:

PHP Constant Usage
++++++++++++++++++

.. meta::
	:description:
		PHP Constant Usage: List of PHP constants being used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Constant Usage
	:twitter:description: PHP Constant Usage: List of PHP constants being used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Constant Usage
	:og:type: article
	:og:description: List of PHP constants being used
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Constants/PhpConstantUsage.html
	:og:locale: en
List of PHP constants being used.

.. code-block:: php
   
   <?php
   
   const MY_CONST = 'Hello';
   
   // PHP_EOL (native PHP Constant)
   // MY_CONST (custom constant, not reported)
   echo PHP_EOL . MY_CONST;
   
   ?>

See also `Predefined Constants <https://www.php.net/manual/en/reserved.constants.php>`_.

Connex PHP features
-------------------

  + `dynamic-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-constant.ini.html>`_
  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/PhpConstantUsage                                                                                                                                                              |
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


