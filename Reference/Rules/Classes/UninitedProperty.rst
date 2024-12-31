.. _classes-uninitedproperty:

.. _uninitialized-property:

Uninitialized Property
++++++++++++++++++++++

.. meta\:\:
	:description:
		Uninitialized Property: Uninitialized properties are not fully bootstrapped at the end of the constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Uninitialized Property
	:twitter:description: Uninitialized Property: Uninitialized properties are not fully bootstrapped at the end of the constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Uninitialized Property
	:og:type: article
	:og:description: Uninitialized properties are not fully bootstrapped at the end of the constructor
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UninitedProperty.html
	:og:locale: en
  Uninitialized properties are not fully bootstrapped at the end of the constructor. 

Properties may be initialized at definition time, along with their visibility and type. Some types are not initialized at definition time, as any object (before PHP 8.2) or resources, so they should be initialized during constructor. At the end of the former, all properties shall have a legit value, and be ready for usage.

PHP 8.1 introduced the possibility to instantiate objects as default value, as long as they only require constant values. This means that those properties may have an object type and a default value.

.. code-block:: php
   
   <?php
   
   class x {
       private $foo = null;
       private $uninited;
       
       function __construct($arg) {
           $this->foo = $args;
           
           // $this->uninited is not inited, nor at definition, nor in constructor
           // it will hold null at the beginning of the next method call
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_
  + `default-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Suggestions
___________

* Remove the property, and move it to another class
* Add an initialisation for this property
* Give the property a neutral value (object or scalar)




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UninitedProperty                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.9                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


