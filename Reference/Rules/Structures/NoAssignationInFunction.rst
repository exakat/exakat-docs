.. _structures-noassignationinfunction:

.. _avoid-large-array-assignation:

Avoid Large Array Assignation
+++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Avoid Large Array Assignation: Avoid setting large arrays to local variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Large Array Assignation
	:twitter:description: Avoid Large Array Assignation: Avoid setting large arrays to local variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Large Array Assignation
	:og:type: article
	:og:description: Avoid setting large arrays to local variables
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NoAssignationInFunction.html
	:og:locale: en
  Avoid setting large arrays to local variables. Such operation is done every time the function is called, and it wastes time. 

This rule applies to constant arrays: when the arrays are dynamically build, with variables or properties, they are not reported here.

There are different ways to avoid this : inject the array, build the array once, use a constant or a global variable. 

The effect on small arrays (less than 10 elements) is not significant. Arrays with 10 elements or more are reported here. The effect is also more important on functions that are called often, or within loops.

.. code-block:: php
   
   <?php
   
   // with constants, for functions
   const ARRAY = array(1,2,3,4,5,6,7,8,9,10,11);
   function foo() {
       $array = ARRAY;
       //more code
   }
   
   // with class constants, for methods 
   class x {
       const ARRAY = array(1,2,3,4,5,6,7,8,9,10,11);
       function foo() {
           $array = self::ARRAY;
           //more code
       }
   }
   
   // with properties, for methods 
   class x {
       private $array = array(1,2,3,4,5,6,7,8,9,10,11);
       
       function foo() {
           $array = $this->array;
           //more code
       }
   }
   
   // injection, leveraging default values
   function foo($array = array(1,2,3,4,5,6,7,8,9,10,11)) {
       //more code
   }
   
   // local cache with static
   function foo() {
       static $array;
       if ($array === null) {
           $array = array(1,2,3,4,5,6,7,8,9,10,11);
       }
       
       //more code
   }
   
   // Avoid creating the same array all the time in a function
   class x {
       function foo() {
           // assign to non local variable is OK. 
           // Here, to a property, though it may be better in a __construct or as default values
           $this->s = array(1,2,3,4,5,6,7,8,9,10,11);
   
           // This is wasting resources, as it is done each time. 
           $array = array(1,2,3,4,5,6,7,8,9,10,11);
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Make the literal a global constant or a class constant
* Make the literal an argument, so it can be injected
* Make the literal an property, with the array as default value
* Make the literal an static variable, with the array as default value




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoAssignationInFunction                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.7                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


