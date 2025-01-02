.. _classes-propertycouldbelocal:

.. _property-could-be-local:

Property Could Be Local
+++++++++++++++++++++++

.. meta::
	:description:
		Property Could Be Local: A property only used in one method may be turned into a local variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Could Be Local
	:twitter:description: Property Could Be Local: A property only used in one method may be turned into a local variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Could Be Local
	:og:type: article
	:og:description: A property only used in one method may be turned into a local variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Could Be Local.html
	:og:locale: en
A property only used in one method may be turned into a local variable.

Public an protected properties are omitted here : they may be modified somewhere else, in the code. This analysis may be upgraded to support those properties, when tracking of such properties becomes available.

Classes where only one non-magic method is available are omitted.

Traits with private properties are processed the same way.

.. code-block:: php
   
   <?php
   
   class x {
       private $foo = 1;
   
       // Magic method, and constructor in particular, are omitted.
       function __construct($foo) {
           $this->foo = $foo;
       }
       
       function bar() {
           $this->foo++;
           
           return $this->foo;
       }
   
       function barbar() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Remove the property and make it an argument in the method
* Use that property elsewhere




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyCouldBeLocal                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mautic-classes-propertycouldbelocal`, :ref:`case-typo3-classes-propertycouldbelocal`                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


