.. _classes-orderofdeclaration:

.. _order-of-declaration:

Order Of Declaration
++++++++++++++++++++

.. meta::
	:description:
		Order Of Declaration: The order used to declare members and methods has a great impact on readability and maintenance.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Order Of Declaration
	:twitter:description: Order Of Declaration: The order used to declare members and methods has a great impact on readability and maintenance
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Order Of Declaration
	:og:type: article
	:og:description: The order used to declare members and methods has a great impact on readability and maintenance
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Order Of Declaration.html
	:og:locale: en
The order used to declare members and methods has a great impact on readability and maintenance. However, practices varies greatly. As usual, being consistent is the most important and useful.

The suggested order is the following : traits, constants, properties, methods. 
Optional characteristics, like final, `static <https://www.php.net/manual/en/language.oop5.static.php>`_... are not specified. Special methods names are not specified.

.. code-block:: php
   
   <?php
   
   class x {
       use traits;
       
       const CONSTANTS = 1;
       const CONSTANTS2 = 1;
       const CONSTANTS3 = 1;
       
       private $property = 2;
       private $property2 = 2;
       private $property3 = 2;
       
       public function foo() {}
       public function foo2() {}
       public function foo3() {}
       public function foo4() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `anonymous-class <https://php-dictionary.readthedocs.io/en/latest/dictionary/anonymous-class.ini.html>`_
  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Always declare class elements (traits, constants, properties, methods) in the same order.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OrderOfDeclaration                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.7                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


