.. _dump-collectsetlocale:

.. _collect-setlocale:

Collect SetLocale
+++++++++++++++++

.. meta\:\:
	:description:
		Collect SetLocale: This rule collects the second argument to all the calls to setlocale().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect SetLocale
	:twitter:description: Collect SetLocale: This rule collects the second argument to all the calls to setlocale()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect SetLocale
	:og:type: article
	:og:description: This rule collects the second argument to all the calls to setlocale()
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectSetLocale.html
	:og:locale: en
  This rule collects the second argument to all the calls to `setlocale() <https://www.php.net/setlocale>`_. This gives an overview of the which special locales are used in the code.

.. code-block:: php
   
   <?php
   
   setlocale(LC_MONEY, 'nl_nl');
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectSetLocale                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
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


