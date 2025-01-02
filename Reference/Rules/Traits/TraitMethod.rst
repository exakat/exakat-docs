.. _traits-traitmethod:

.. _trait-methods:

Trait Methods
+++++++++++++

.. meta::
	:description:
		Trait Methods: List the names of the methods in a trait.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Trait Methods
	:twitter:description: Trait Methods: List the names of the methods in a trait
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Trait Methods
	:og:type: article
	:og:description: List the names of the methods in a trait
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Trait Methods.html
	:og:locale: en
List the names of the methods in a trait. 

.. code-block:: php
   
   <?php
   
   trait t {
       private $property = 1;
       
       // This is a trait method name
       function foo() {
           // This is not a trait method 
           return function($a) { return $a + 1; }
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_
  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/TraitMethod                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


