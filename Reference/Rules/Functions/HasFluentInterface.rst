.. _functions-hasfluentinterface:


.. _method-has-fluent-interface:

Method Has Fluent Interface
+++++++++++++++++++++++++++

.. meta::
	:description:
		Method Has Fluent Interface: Mark a method when it only returns $this.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Has Fluent Interface
	:twitter:description: Method Has Fluent Interface: Mark a method when it only returns $this
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Has Fluent Interface
	:og:type: article
	:og:description: Mark a method when it only returns $this
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Has Fluent Interface.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/HasFluentInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/HasFluentInterface.html","name":"Method Has Fluent Interface","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark a method when it only returns $this","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Has Fluent Interface.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mark a method when it only returns `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_.

Fluent interfaces allows for chaining methods calls. This implies that `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ is always returned, so that the next method call is done on the same object.

.. code-block:: php
   
   <?php
   
   $object = new foo();
   $object->this()
          ->is()
          ->a()
          ->fluent()
          ->interface();
          
   class foo {
       function this() {
           // doSomething
           return $this;
       }
   
       function is() {
           // doSomethingElse
           return $this;
       }
       
       /// Etc. for a(), fluent(), interface()...
   }
   
   ?>

See also `Fluent Interfaces in PHP <http://mikenaberezny.com/2005/12/20/fluent-interfaces-in-php/>`_ and `Fluent Interfaces are Evil <https://ocramius.github.io/blog/fluent-interfaces-are-evil/>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/HasFluentInterface                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


