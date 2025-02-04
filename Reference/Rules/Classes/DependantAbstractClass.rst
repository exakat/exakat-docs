.. _classes-dependantabstractclass:


.. _dependant-abstract-classes:

Dependant Abstract Classes
++++++++++++++++++++++++++

.. meta::
	:description:
		Dependant Abstract Classes: Abstract classes should be autonomous.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dependant Abstract Classes
	:twitter:description: Dependant Abstract Classes: Abstract classes should be autonomous
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dependant Abstract Classes
	:og:type: article
	:og:description: Abstract classes should be autonomous
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dependant Abstract Classes.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DependantAbstractClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DependantAbstractClass.html","name":"Dependant Abstract Classes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Abstract classes should be autonomous","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dependant Abstract Classes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Abstract classes should be autonomous. It is recommended to avoid depending on methods, constant or properties that should be made available in inheriting classes, without explicitly abstracting them.

The following abstract classes make usage of constant, methods and properties, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not, that are not defined in the class. This means the inheriting classes must provide those constants, methods and properties, but there is no way to enforce this. 

This may also lead to dead code : when the abstract class is removed, the host class have unused properties and methods.

.. code-block:: php
   
   <?php
   
   // autonomous abstract class : all it needs is within the class
   abstract class c {
       private $p = 0;
       
       function foo() {
           return ++$this->p;
       }
   }
   
   // dependant abstract class : the inheriting classes needs to provide some properties or methods
   abstract class c2 {
       function foo() {
           // $p must be provided by the extending class
           return ++$this->p;
       }
   }
   
   class c3 extends c2 {
       private $p = 0;
   }
   ?>

See also :ref:`Dependant Trait <dependant-trait>`.

Connex PHP features
-------------------

  + `Abstract Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Make the class only use its own resources
* Split the class in autonomous classes
* Add local property definitions to make the class independent




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DependantAbstractClass                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.6                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


