.. _classes-unitializedproperties:

.. _unitialized-properties:

Unitialized Properties
++++++++++++++++++++++

.. meta::
	:description:
		Unitialized Properties: Properties that are not initialized in the constructor, nor at definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unitialized Properties
	:twitter:description: Unitialized Properties: Properties that are not initialized in the constructor, nor at definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unitialized Properties
	:og:type: article
	:og:description: Properties that are not initialized in the constructor, nor at definition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unitialized Properties.html
	:og:locale: en
Properties that are not initialized in the constructor, nor at definition. 

With the above class, when m() is accessed right after instantiation, there will be a missing property. 
Using default values at property definition, or setting default values in the constructor ensures that the created object is consistent.

.. code-block:: php
   
   <?php
   
   class X {
       private $i1 = 1, $i2;
       protected $u1, $u2;
       
       function __construct() {
           $this->i2 = 1 + $this->u2;
       }
       
       function m() {
           echo $this->i1, $this->i2, $this->u1, $this->u2;
       }
   }
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Add an explicit initialization for each property.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnitializedProperties                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-classes-unitializedproperties`                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


