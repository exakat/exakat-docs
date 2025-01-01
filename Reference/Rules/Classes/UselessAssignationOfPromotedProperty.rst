.. _classes-uselessassignationofpromotedproperty:

.. _useless-assignation-of-promoted-property:

Useless Assignation Of Promoted Property
++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Useless Assignation Of Promoted Property: Promoted properties save the assignation of constructor argument to the property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Assignation Of Promoted Property
	:twitter:description: Useless Assignation Of Promoted Property: Promoted properties save the assignation of constructor argument to the property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Assignation Of Promoted Property
	:og:type: article
	:og:description: Promoted properties save the assignation of constructor argument to the property
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UselessAssignationOfPromotedProperty.html
	:og:locale: en
Promoted properties save the assignation of constructor argument to the property. It is useless to do it with that syntax, and in the constructor too.

.. code-block:: php
   
   <?php
   
   class x {
   	private $b;
   	
   	function __construct(private $a,
   						 $b,						 
   						 ) {
   		// This is already done with the promoted property
   		$this->a = $a;
   
   		// This is the traditional way (up to PHP 8.0)
   		$this->b = $b;
   		}
   }
   
   ?>
Connex PHP features
-------------------

  + `promoted-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/promoted-property.ini.html>`_


Suggestions
___________

* Remove the assignation in the constructor




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessAssignationOfPromotedProperty                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


