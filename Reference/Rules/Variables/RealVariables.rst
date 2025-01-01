.. _variables-realvariables:

.. _real-variables:

Real Variables
++++++++++++++

.. meta::
	:description:
		Real Variables: Inventory of real variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Real Variables
	:twitter:description: Real Variables: Inventory of real variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Real Variables
	:og:type: article
	:og:description: Inventory of real variables
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/RealVariables.html
	:og:locale: en
Inventory of real variables. Global, `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ and property declarations are skipped here. 
This is a refined version of a search on ``T_VARIABLE`` token.

.. code-block:: php
   
   <?php
   
   $realVariable = 1;
   
   class foo {
       private $property;        // not a variable
       
       private function bar() {
           global $global;       // not a variable
           static $static;       // not a variable
           
       }
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/RealVariables                                                                                                 |
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


