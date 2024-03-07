.. _classes-tostringpss:

.. _magic-visibility:

Magic Visibility
++++++++++++++++

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


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/toStringPss                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | visibility, magic-method                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


