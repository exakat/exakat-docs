.. _interfaces-interfaceusage:

.. _interfaces-usage:

Interfaces Usage
++++++++++++++++

.. meta::
	:description:
		Interfaces Usage: List of used interfaces.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Interfaces Usage
	:twitter:description: Interfaces Usage: List of used interfaces
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Interfaces Usage
	:og:type: article
	:og:description: List of used interfaces
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Interfaces Usage.html
	:og:locale: en
List of used interfaces.

Interfaces are used when mentioned in a class or another interface, with implements keyword; they are used in `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ expression, in typehints and class constant.

.. code-block:: php
   
   <?php
   
   // interface definition
   interface i {
       const I = 2;
   }
   
   // interface extension 
   interface i2 extends i {}
   
   // interface implementation 
   class foo implements i {}
   
   $foo = new foo();
   
   var_dump($foo instanceof i);
   
   function bar( i $arg) { }
   bar($foo);
   
   // in class constant
   echo i::I;
   
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/InterfaceUsage                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


