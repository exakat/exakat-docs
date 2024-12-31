.. _complete-phpnativereference:

.. _php-native-reference-variable:

Php Native Reference Variable
+++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Php Native Reference Variable: Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Php Native Reference Variable
	:twitter:description: Php Native Reference Variable: Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Php Native Reference Variable
	:og:type: article
	:og:description: Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/PhpNativeReference.html
	:og:locale: en
  Native functions, such as `sort() <https://www.php.net/sort>`_ (first argument), or `preg_match_all() <https://www.php.net/preg_match_all>`_ (third argument), use reference.

.. code-block:: php
   
   <?php
   
   $a = [3,1,2];
   sort($a);
   $a === [1,2,3];
   
   ?>
Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/PhpNativeReference                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


