.. _patterns-courrierantipattern:


.. _courier-anti-pattern:

Courier Anti-Pattern
++++++++++++++++++++

.. meta::
	:description:
		Courier Anti-Pattern: The courier anti-pattern is the storage of a dependency by a class, in order to create an instance that requires this dependency.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Courier Anti-Pattern
	:twitter:description: Courier Anti-Pattern: The courier anti-pattern is the storage of a dependency by a class, in order to create an instance that requires this dependency
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Courier Anti-Pattern
	:og:type: article
	:og:description: The courier anti-pattern is the storage of a dependency by a class, in order to create an instance that requires this dependency
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Courier Anti-Pattern.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/CourrierAntiPattern.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/CourrierAntiPattern.html","name":"Courier Anti-Pattern","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The courier anti-pattern is the storage of a dependency by a class, in order to create an instance that requires this dependency","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Courier Anti-Pattern.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The courier anti-pattern is the storage of a dependency by a class, in order to create an instance that requires this dependency.

The class itself doesn't actually need this dependency, but has a dependency to a class that requires it. 
The alternative here is to inject Foo instead of Bar.

.. code-block:: php
   
   <?php
   
   // The foo class requires bar
   class Foo {
       public function __construct(Bar $b) {
       }
   }
   
   // Class A doesn't depends on Bar, but depends on Foo
   // Class A never uses Bar, but only uses Foo.
   class A {
       private $courier;
   
       public function __construct(Bar $courier) {
           $this->courier = $courier;       
       }
   
       public function Afoo() {
           $b = new Foo($this->courier);
       }
   
   }
   
   ?>

See also `Courier Anti-pattern <https://r.je/oop-courier-anti-pattern.html>`_.

Connex PHP features
-------------------

  + `Design Pattern <https://php-dictionary.readthedocs.io/en/latest/dictionary/pattern.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/CourrierAntiPattern                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


