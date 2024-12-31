.. _extensions-extxdebug:

.. _ext-xdebug:

ext/xdebug
++++++++++

.. meta\:\:
	:description:
		ext/xdebug: Xdebug extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xdebug
	:twitter:description: ext/xdebug: Xdebug extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xdebug
	:og:type: article
	:og:description: Xdebug extension
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extxdebug.html
	:og:locale: en
  Xdebug extension.

The Xdebug is a extension PHP which provides debugging and profiling capabilities.

.. code-block:: php
   
   <?php
   class Strings
   {
       static function fix_string($a)
       {
           echo
               xdebug_call_class().
               "::".
               xdebug_call_function().
               " is called at ".
               xdebug_call_file().
               ":".
               xdebug_call_line();
       }
   }
   
   $ret = Strings::fix_string( 'Derick' );
   ?>

See also `Xdebug <https://xdebug.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxdebug                                                                                                                                                                    |
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


