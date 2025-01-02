.. _constants-customconstantusage:

.. _custom-constant-usage:

Custom Constant Usage
+++++++++++++++++++++

.. meta::
	:description:
		Custom Constant Usage: The code is using constants that are not defined in PHP extensions or PHP itself.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Custom Constant Usage
	:twitter:description: Custom Constant Usage: The code is using constants that are not defined in PHP extensions or PHP itself
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Custom Constant Usage
	:og:type: article
	:og:description: The code is using constants that are not defined in PHP extensions or PHP itself
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Custom Constant Usage.html
	:og:locale: en
The code is using constants that are not defined in PHP extensions or PHP itself. This may lead to a fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // display MY_CONSTANT : MY_CONSTANT is a user constant.
   echo MY_CONSTANT;
   
   // display PHP version : PHP_VERSION is a native PHP constant.
   echo PHP_VERSION;
   
   // MY_CONSTANT definition. 
   const MY_CONSTANT;
   
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CustomConstantUsage                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
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


