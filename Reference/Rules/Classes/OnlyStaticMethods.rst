.. _classes-onlystaticmethods:

.. _only-static-methods-class:

Only Static Methods Class
+++++++++++++++++++++++++

.. meta\:\:
	:description:
		Only Static Methods Class: This rule marks a class that only contains static methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Only Static Methods Class
	:twitter:description: Only Static Methods Class: This rule marks a class that only contains static methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Only Static Methods Class
	:og:type: article
	:og:description: This rule marks a class that only contains static methods
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/OnlyStaticMethods.html
	:og:locale: en
  This rule marks a class that only contains `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods. Such classes are tool classes, with definition of methods that can be called without an object. This is akin to functions, with autoloading possibilities.

.. code-block:: php
   
   <?php
   
   class x {
       static function foo() {}
       static function goo() {}
       static function hoo() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OnlyStaticMethods                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


