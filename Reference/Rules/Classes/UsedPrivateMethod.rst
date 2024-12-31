.. _classes-usedprivatemethod:

.. _used-private-methods:

Used Private Methods
++++++++++++++++++++

.. meta\:\:
	:description:
		Used Private Methods: List of all private methods that are used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Private Methods
	:twitter:description: Used Private Methods: List of all private methods that are used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Private Methods
	:og:type: article
	:og:description: List of all private methods that are used
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UsedPrivateMethod.html
	:og:locale: en
  List of all private methods that are used.

Protected methods, in a standalone class, are also included.

.. code-block:: php
   
   <?php
   
   class Foo {
       // Those methods are used
       private function method() {}
       private static function staticMethod() {}
   
       // Those methods are not used
       private function unusedMethod() {}
       private static function staticUnusedMethod() {}
       
       public function bar() {
           self::staticMethod();
           $this->method();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedPrivateMethod                                                                                               |
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


