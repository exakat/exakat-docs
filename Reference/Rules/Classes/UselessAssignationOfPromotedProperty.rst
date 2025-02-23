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
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Assignation Of Promoted Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessAssignationOfPromotedProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessAssignationOfPromotedProperty.html","name":"Useless Assignation Of Promoted Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Promoted properties save the assignation of constructor argument to the property","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Assignation Of Promoted Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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

  + `Promoted Properties <https://php-dictionary.readthedocs.io/en/latest/dictionary/promoted-property.ini.html>`_


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


