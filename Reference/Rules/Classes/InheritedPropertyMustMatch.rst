.. _classes-inheritedpropertymustmatch:


.. _inherited-property-type-must-match:

Inherited Property Type Must Match
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Inherited Property Type Must Match: Properties that are inherited between classes must match.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inherited Property Type Must Match
	:twitter:description: Inherited Property Type Must Match: Properties that are inherited between classes must match
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inherited Property Type Must Match
	:og:type: article
	:og:description: Properties that are inherited between classes must match
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Inherited Property Type Must Match.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/InheritedPropertyMustMatch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/InheritedPropertyMustMatch.html","name":"Inherited Property Type Must Match","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Properties that are inherited between classes must match","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Inherited Property Type Must Match.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Properties that are inherited between classes must match. 

This affect public and protected properties. Private properties are immune to this rule, as they actually are distinct properties.

.. code-block:: php
   
   <?php
   
   class A {
       private A $a;
       protected array $b;
       public $c;
   }
   
   class B extends A {
       private A $a;       // OK, as it is private
       protected int $b;   // type must match with the previous definition
       public $c;          // no type behaves just like a type : it must match too.
   }
   
   ?>

See also `Properties <https://www.php.net/manual/en/language.oop5.properties.php>`_.

Related PHP errors 
-------------------

  + `Type of b::$a must not be defined (as in class a) <https://php-errors.readthedocs.io/en/latest/messages/type-of-%25s%3A%3A%24%25s-must-not-be-defined-%28as-in-class-%25s%29.html>`_
  + `Type of b::$a must be array (as in class a) <https://php-errors.readthedocs.io/en/latest/messages/type-of-%25s%3A%3A%24%25s-must-be-%25s%25s-%28as-in-class-%25s%29.html>`_



Connex PHP features
-------------------

  + `Inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_
  + `Properties <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Remove the definition in the child class
* Synchronize the definition of the property in the child class




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/InheritedPropertyMustMatch                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


