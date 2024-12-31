.. _structures-usedebug:

.. _use-debug:

Use Debug
+++++++++

.. meta\:\:
	:description:
		Use Debug: The code source includes calls to debug functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Debug
	:twitter:description: Use Debug: The code source includes calls to debug functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Debug
	:og:type: article
	:og:description: The code source includes calls to debug functions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UseDebug.html
	:og:locale: en
  The code source includes calls to debug functions.

The following debug functions and libraries are reported : 

* `Aronduby Dump <https://github.com/aronduby/dump>`_
* `Cakephp Debug Toolbar <https://github.com/cakephp/debug_kit>`_
* `Kint <https://github.com/kint-php/kint>`_
* `Krumo <https://github.com/mmucklo/krumo>`_
* `Nette tracy <https://tracy.nette.org/>`_
* `php-debugbar <https://github.com/maximebf/php-debugbar>`_
* PHP native functions : `print_r() <https://www.php.net/print_r>`_, `var_dump() <https://www.php.net/var_dump>`_, `debug_backtrace() <https://www.php.net/debug_backtrace>`_, `debug_print_backtrace() <https://www.php.net/debug_print_backtrace>`_, `debug_zval_dump() <https://www.php.net/debug_zval_dump>`_
* `Symfony debug <https://symfony.com/doc/current/components/debug.html>`_
* `Wordpress debug <https://codex.wordpress.org/Debugging_in_WordPress>`_
* `Xdebug <https://xdebug.org/>`_
* `Zend debug <https://github.com/zendframework/zend-debug>`_

.. code-block:: php
   
   <?php
   
   // Example with Zend Debug
   Zend\Debug\Debug::dump($var, $label = null, $echo = true);
   
   ?>
Connex PHP features
-------------------

  + `debug <https://php-dictionary.readthedocs.io/en/latest/dictionary/debug.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseDebug                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.4                                                                                                                                                                                  |
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


