.. _classes-hasfluentinterface:


.. _class-has-fluent-interface:

Class Has Fluent Interface
++++++++++++++++++++++++++

.. meta::
	:description:
		Class Has Fluent Interface: Mark a class as such when it contains at least one fluent method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Has Fluent Interface
	:twitter:description: Class Has Fluent Interface: Mark a class as such when it contains at least one fluent method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Has Fluent Interface
	:og:type: article
	:og:description: Mark a class as such when it contains at least one fluent method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Has Fluent Interface.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/HasFluentInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/HasFluentInterface.html","name":"Class Has Fluent Interface","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Mark a class as such when it contains at least one fluent method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Has Fluent Interface.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mark a class as such when it contains at least one fluent method. A fluent method is a method that returns `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_, for chaining.

.. code-block:: php
   
   <?php
   
   class foo {
       private $count = 0;
   
       function a() {
           ++$this->count;
           return $this;
       }
   
       function b() {
           $this->count += 2;
           return $this;
       }
   
       function c() {
           return $this->count;
       }
   }
   
   $bar = new foo();
   print $bar->a()
             ->b()
             ->c();
   
   // display 3 (1 + 2).
   
   ?>

See also `Fluent interface are evil <https://ocramius.github.io/blog/fluent-interfaces-are-evil/>`_, `The basics of Fluent interfaces in PHP <https://tournasdimitrios1.wordpress.com/2011/04/11/the-basics-of-fluent-interfaces-in-php/>`_ and `FluentInterface <https://martinfowler.com/bliki/FluentInterface.html>`_.

Connex PHP features
-------------------

  + `fluent-interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/fluent-interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/HasFluentInterface                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


