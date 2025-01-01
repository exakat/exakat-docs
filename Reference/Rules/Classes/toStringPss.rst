.. _classes-tostringpss:

.. _magic-visibility:

Magic Visibility
++++++++++++++++

.. meta::
	:description:
		Magic Visibility: Magic methods must be declared with public visibility.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Magic Visibility
	:twitter:description: Magic Visibility: Magic methods must be declared with public visibility
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Magic Visibility
	:og:type: article
	:og:description: Magic methods must be declared with public visibility
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/toStringPss.html
	:og:locale: en
Magic methods must be declared with public visibility. They cannot be private or protected.

Magic methods cannot be declared as `static <https://www.php.net/manual/en/language.oop5.static.php>`_. They are always associated with an instance of a class and cannot be called statically.

.. code-block:: php
   
   <?php
   
   class foo{
       // magic method must bt public and non-static
       public static function __clone($name) {    }
   
       // magic method can't be private
       private function __get($name) {    }
   
       // magic method can't be protected
       private function __set($name, $value) {    }
   
       // magic method can't be static
       public static function __isset($name) {    }
   }
   
   ?>

See also `Magic methods <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `PHP Magic Methods Explained <https://atakde.medium.com/php-magic-methods-explained-bac7053c007d>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/The+magic+method+x%3A%3A__call%28%29+must+have+public+visibility.html>`_



Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_
  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/toStringPss                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


