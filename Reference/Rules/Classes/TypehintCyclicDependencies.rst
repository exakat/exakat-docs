.. _classes-typehintcyclicdependencies:


.. _di-cyclic-dependencies:

DI Cyclic Dependencies
++++++++++++++++++++++

.. meta::
	:description:
		DI Cyclic Dependencies: When injecting dependencies, classes that mutually depend on each other is a code smell.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: DI Cyclic Dependencies
	:twitter:description: DI Cyclic Dependencies: When injecting dependencies, classes that mutually depend on each other is a code smell
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: DI Cyclic Dependencies
	:og:type: article
	:og:description: When injecting dependencies, classes that mutually depend on each other is a code smell
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/DI Cyclic Dependencies.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/TypehintCyclicDependencies.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/TypehintCyclicDependencies.html","name":"DI Cyclic Dependencies","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When injecting dependencies, classes that mutually depend on each other is a code smell","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/DI Cyclic Dependencies.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When injecting dependencies, classes that mutually depend on each other is a code smell. 

Dependency injection should be organized as an acyclic tree-like structure

.. code-block:: php
   
   <?php
   
   // Classes A and B depends on each other. 
   class A {
       protected $b;
   
       public function __construct(B $b) {
           $this->b = $b;
       }
   }
   
   class B {
       public $a;
   
       protected function setA(A $a) {
           $this->a = $a;
       }
   }
   ?>

See also `Dependency Injection Smells <http://seregazhuk.github.io/2017/05/04/di-smells/>`_.

Connex PHP features
-------------------

  + `Injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/injection.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TypehintCyclicDependencies                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


