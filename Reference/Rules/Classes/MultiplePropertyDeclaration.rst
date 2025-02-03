.. _classes-multiplepropertydeclaration:


.. _multiple-property-declaration:

Multiple Property Declaration
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Multiple Property Declaration: The same property is declared in various classes, at least two, in the same class hierarchy.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Multiple Property Declaration

	:twitter:description: Multiple Property Declaration: The same property is declared in various classes, at least two, in the same class hierarchy

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Multiple Property Declaration

	:og:type: article

	:og:description: The same property is declared in various classes, at least two, in the same class hierarchy

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Property Declaration.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MultiplePropertyDeclaration.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MultiplePropertyDeclaration.html","name":"Multiple Property Declaration","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The same property is declared in various classes, at least two, in the same class hierarchy","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Property Declaration.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The same property is declared in various classes, at least two, in the same class hierarchy. The declarations must be compatible one another, and one of them should be sufficient. 

Generally, the higher declaration should be the one to stay. 

Keeping one definition makes it clear which class is responsible for that property. It also keep the code more flexible in case of an update on the property: only one place to change it.

.. code-block:: php
   
   <?php
   
   class x {
   	// redeclared in y
   	public $p = 1;
   	
   	// declared only in x;
   	public $q;
   }
   
   class y extends x {
   	// redeclared in x
   	public $p = 2;
   
   	// declared only in y;
   	public $q;
   }
   
   ?>
Connex PHP features
-------------------

  + `dry <https://php-dictionary.readthedocs.io/en/latest/dictionary/dry.ini.html>`_


Suggestions
___________

* Remove all but one of the declarations
* Change the name of some of the properties, to keep their meaning separate




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MultiplePropertyDeclaration                                                                                      |
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
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


