.. _classes-insufficientpropertytypehint:

.. _insufficient-property-type:

Insufficient Property Type
++++++++++++++++++++++++++

.. meta::
	:description:
		Insufficient Property Type: The type used for a class property doesn't cover all it usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Insufficient Property Type
	:twitter:description: Insufficient Property Type: The type used for a class property doesn't cover all it usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Insufficient Property Type
	:og:type: article
	:og:description: The type used for a class property doesn't cover all it usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Insufficient Property Type.html
	:og:locale: en
The type used for a class property doesn't cover all it usage.

The type is insufficient when a undefined method or constant is called, or if members are accessed while the type is an interface.

This analysis relies on typed properties, as introduced in PHP 7.4. It also relies on typed assignations at construct time : the type of the assigned argument will be used as the property type. Getters and setters are not considered here.

.. code-block:: php
   
   <?php
   
   class A {
       function a1() {}
   }
   
   // PHP 7.4 and more recent
   class B {
       private A $a = null;
       
       function b2() {
           // this method is available in A
           $this->a->a1();
           // this method is NOT available in A
           $this->a->a2();
       }
   }
   
   // Supported by all PHP versions
   class C {
       private $a = null;
   
       function __construct(A $a) {
           $this->a = $a;
       }
       
       function b2() {
           // this method is available in A
           $this->a->a1();
           // this method is NOT available in A
           $this->a->a2();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Change the type to match the actual usage of the object in the class. 




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/InsufficientPropertyTypehint                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


