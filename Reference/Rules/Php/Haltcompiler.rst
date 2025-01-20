.. _php-haltcompiler:

.. _\_\_halt\_compiler:

__halt_compiler
+++++++++++++++

.. meta::
	:description:
		__halt_compiler: This rule reports ``__halt_compiler()`` usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: __halt_compiler
	:twitter:description: __halt_compiler: This rule reports ``__halt_compiler()`` usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: __halt_compiler
	:og:type: article
	:og:description: This rule reports ``__halt_compiler()`` usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/__halt_compiler.html
	:og:locale: en
This rule reports ``__halt_compiler()`` usage. This function is rarely used, beside with `Phar <https://www.php.net/phar>`_ archives, or to deliver both PHP code and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ binary.

.. code-block:: php
   
   <?php
   
   // open this file
   $fp = fopen(__FILE__, 'r');
   
   // seek file pointer to data
   fseek($fp, __COMPILER_HALT_OFFSET__);
   
   // and output it
   var_dump(stream_get_contents($fp));
   
   // the end of the script execution
   __halt_compiler(); the installation data (eg. tar, gz, PHP, etc.)
   
   ?>

See also `__halt_compiler <https://www.php.net/manual/en/function.halt-compiler.php>`__.

Connex PHP features
-------------------

  + `halt-compiler <https://php-dictionary.readthedocs.io/en/latest/dictionary/halt-compiler.ini.html>`_
  + `phar <https://php-dictionary.readthedocs.io/en/latest/dictionary/phar.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Haltcompiler                                                                                                                                                                        |
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


