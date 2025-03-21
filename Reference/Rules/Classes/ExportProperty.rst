.. _classes-exportproperty:


.. _property-export:

Property Export
+++++++++++++++

.. meta::
	:description:
		Property Export: With a reference, it is possible to export a property and modify it from the outside.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Export
	:twitter:description: Property Export: With a reference, it is possible to export a property and modify it from the outside
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Export
	:og:type: article
	:og:description: With a reference, it is possible to export a property and modify it from the outside
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Export.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ExportProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ExportProperty.html","name":"Property Export","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"With a reference, it is possible to export a property and modify it from the outside","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Property Export.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

With a reference, it is possible to export a property and modify it from the outside. This requires the handling of the reference with a method and a variable. 

The `result <https://www.php.net/result>`_ is a suprising modification of the original object, even if its visibility is private. 

.. code-block:: php
   
   <?php
   
   class x {
   	private $p = [];
   	
   	function &foo() {
   		return $this->p;
   	}
   
   	function print() {
   		print_r($this->p);
   	}
   }
   
   $x = new x();
   $export = &$x->foo();
   $export[] = 2;
   
   $x->print();
   // property $p has been modified in $x
   // $x->p === [2]; 
   
   ?>

Suggestions
___________

* Avoid modifying an object without its knowledge




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ExportProperty                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


