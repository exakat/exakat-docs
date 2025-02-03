.. _traits-incompatibleproperty:

.. _incompatible-property-between-class-and-trait:

Incompatible Property Between Class And Trait
+++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Incompatible Property Between Class And Trait: Reports a property definition that doesn't fit the importing class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incompatible Property Between Class And Trait
	:twitter:description: Incompatible Property Between Class And Trait: Reports a property definition that doesn't fit the importing class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incompatible Property Between Class And Trait
	:og:type: article
	:og:description: Reports a property definition that doesn't fit the importing class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incompatible Property Between Class And Trait.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/IncompatibleProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/IncompatibleProperty.html","name":"Incompatible Property Between Class And Trait","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Reports a property definition that doesn't fit the importing class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Incompatible Property Between Class And Trait.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Reports a property definition that doesn't fit the importing class. The property definition should be identical in the trait and in the class. 

.. code-block:: php
   
   <?php
   
   trait T { 
   	private Invalid $property1; 
   
   	private Valid $property2; 
   }
   
   class XT { 
   	use T; 
   	
   	// This is incompatible with the trait
   	private OtherType $property1; 
   
   	// This is compatible with the trait
   	private Valid $property2; 
   }
   
   ?>
Related PHP errors 
-------------------

  + `theClass and theTrait define the same property ($property) in the composition of theClass. However, the definition differs and is considered incompatible. <https://php-errors.readthedocs.io/en/latest/messages/%25s-and-%25s-define-the-same-constant-%28%25s%29-in-the-composition-of-%25s.-however%2C-the-definition-differs-and-is-considered-incompatible.-class-was-composed.html>`_



Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Make sure the property is defined identically in the class and the trait.
* Change the property definition in the class and make it distinct with the one in the trait.
* Change the property definition in the trait and make it distinct with the one in the class.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/IncompatibleProperty                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


