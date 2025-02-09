.. _structures-usedebug:


.. _use-debug:

Use Debug
+++++++++

.. meta::
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
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Debug.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseDebug.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseDebug.html","name":"Use Debug","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The code source includes calls to debug functions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Debug.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The code source includes calls to debug functions.

The following debug functions and libraries are reported : 

* `Aronduby Dump <https://github.`com <https://www.php.net/com>`_/aronduby/dump>`_
* `Cakephp Debug Toolbar <https://github.`com <https://www.php.net/com>`_/cakephp/debug_kit>`_
* `Kint <https://github.`com <https://www.php.net/com>`_/kint-php/kint>`_
* `Krumo <https://github.`com <https://www.php.net/com>`_/mmucklo/krumo>`_
* `Nette tracy <https://tracy.nette.org/>`_
* `php-debugbar <https://github.`com <https://www.php.net/com>`_/maximebf/php-debugbar>`_
* PHP native functions : `print_r() <https://www.php.net/print_r>`_, `var_dump() <https://www.php.net/var_dump>`_, `debug_backtrace() <https://www.php.net/debug_backtrace>`_, `debug_print_backtrace() <https://www.php.net/debug_print_backtrace>`_, `debug_zval_dump() <https://www.php.net/debug_zval_dump>`_
* `Symfony debug <https://symfony.`com <https://www.php.net/com>`_/doc/current/components/debug.html>`_
* `Wordpress debug <https://codex.wordpress.org/Debugging_in_WordPress>`_
* `Xdebug <https://xdebug.org/>`_
* `Zend debug <https://github.`com <https://www.php.net/com>`_/zendframework/zend-debug>`_

.. code-block:: php
   
   <?php
   
   // Example with Zend Debug
   Zend\Debug\Debug::dump($var, $label = null, $echo = true);
   
   ?>
Connex PHP features
-------------------

  + `Debugger <https://php-dictionary.readthedocs.io/en/latest/dictionary/debug.ini.html>`_


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


