.. _patterns-dependencyinjection:

.. _dependency-injection:

Dependency Injection
++++++++++++++++++++

.. meta::
	:description:
		Dependency Injection: A dependency injection is a typehinted argument, that is stored in a property by the constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dependency Injection
	:twitter:description: Dependency Injection: A dependency injection is a typehinted argument, that is stored in a property by the constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dependency Injection
	:og:type: article
	:og:description: A dependency injection is a typehinted argument, that is stored in a property by the constructor
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dependency Injection.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/DependencyInjection.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/DependencyInjection.html","name":"Dependency Injection","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A dependency injection is a typehinted argument, that is stored in a property by the constructor","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dependency Injection.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A dependency injection is a typehinted argument, that is stored in a property by the constructor.

.. code-block:: php
   
   <?php
   
   // Classic dependency injection 
   class foo {
       private $bar;
   
       public function __construct(Bar $bar) {
           $this->bar = $bar;
       }
   
       public function doSomething($args) {
           return $this->bar->barbar($args);
       }
   }
   
   // Without typehint, this is not a dependency injection
   class foo {
       private $bar;
   
       public function __construct($bar) {
           $this->bar = $bar;
       }
   }
   
   ?>

See also `Understanding Dependency Injection <http://php-di.org/doc/understanding-di.html>`_.

Connex PHP features
-------------------

  + `dependency-injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/dependency-injection.ini.html>`_
  + `pattern <https://php-dictionary.readthedocs.io/en/latest/dictionary/pattern.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/DependencyInjection                                                                                                                                                            |
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


