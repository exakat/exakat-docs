.. _php-triggererrorusage:

.. _trigger-errors:

Trigger Errors
++++++++++++++

.. meta::
	:description:
		Trigger Errors: List of situations where user errors are triggered.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Trigger Errors
	:twitter:description: Trigger Errors: List of situations where user errors are triggered
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Trigger Errors
	:og:type: article
	:og:description: List of situations where user errors are triggered
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/TriggerErrorUsage.html
	:og:locale: en
List of situations where user errors are triggered.

PHP errors are triggered with `trigger_error() <https://www.php.net/trigger_error>`_.

.. code-block:: php
   
   <?php
   if ($divisor == 0) {
       trigger_error('Cannot divide by zero', E_USER_ERROR);
   }
   ?>

See also `trigger_error <https://www.php.net/trigger_error>`_.

Connex PHP features
-------------------

  + `error <https://php-dictionary.readthedocs.io/en/latest/dictionary/error.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/TriggerErrorUsage                                                                                                                                                                   |
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


