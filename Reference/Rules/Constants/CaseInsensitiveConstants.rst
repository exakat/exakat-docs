.. _constants-caseinsensitiveconstants:

.. _case-insensitive-constants:

Case Insensitive Constants
++++++++++++++++++++++++++

.. meta::
	:description:
		Case Insensitive Constants: PHP constants used to be able to be case insensitive, when defined with define() and the third argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Case Insensitive Constants
	:twitter:description: Case Insensitive Constants: PHP constants used to be able to be case insensitive, when defined with define() and the third argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Case Insensitive Constants
	:og:type: article
	:og:description: PHP constants used to be able to be case insensitive, when defined with define() and the third argument
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Constants/CaseInsensitiveConstants.html
	:og:locale: en
PHP constants used to be able to be case insensitive, when defined with `define() <https://www.php.net/define>`_ and the third argument.

This feature is deprecated since PHP 7.3 and is removed since PHP 8.0.

.. code-block:: php
   
   <?php
   
   // case sensitive
   define('A', 1);
   
   // case insensitive
   define('B', 1, true);
   
   echo A;
   // This is not possible
   //echo a;
   
   // both possible
   echo B;
   echo b;
   
   ?>

See also `define <https://www.php.net/define>`_.

Related PHP errors 
-------------------

  + `define(): Declaration of case-insensitive constants is deprecated <https://php-errors.readthedocs.io/en/latest/messages/define%5C%28%5C%29%5C%3A-declaration-of-case-insensitive-constants-is-deprecated.html>`_
  + `Argument #3 ($case_insensitive) is ignored since declaration of case-insensitive constants is no longer supported <https://php-errors.readthedocs.io/en/latest/messages/define%5C%28%5C%29%5C%3A-argument-%233-%5C%28%24case_insensitive%5C%29-is-ignored-since-declaration-of-case-insensitive-constants-is-no-longer-supported.html>`_



Connex PHP features
-------------------

  + `dynamic-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-constant.ini.html>`_
  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CaseInsensitiveConstants                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`Deprecated <ruleset-Deprecated>`      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


