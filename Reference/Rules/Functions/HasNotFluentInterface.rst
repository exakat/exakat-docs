.. _functions-hasnotfluentinterface:


.. _method-is-not-for-fluent-interface:

Method Is Not For Fluent Interface
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Method Is Not For Fluent Interface: Mark a method when it contains at least one return that doesn't return $this.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Is Not For Fluent Interface
	:twitter:description: Method Is Not For Fluent Interface: Mark a method when it contains at least one return that doesn't return $this
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Is Not For Fluent Interface
	:og:type: article
	:og:description: Mark a method when it contains at least one return that doesn't return $this
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Is Not For Fluent Interface.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/HasNotFluentInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/HasNotFluentInterface.html","name":"Method Is Not For Fluent Interface","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark a method when it contains at least one return that doesn't return $this","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Is Not For Fluent Interface.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mark a method when it contains at least one return that doesn't return `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_. Such method cannot be used for fluent interface, which always require the current object to be returned. 

`Null <https://www.php.net/`null <https://www.php.net/null>`_>`_ is not accepted here: it would `break <https://www.php.net/manual/en/control-structures.break.php>`_ the execution of the method call chains if it was returned. 


.. code-block:: php
   
   <?php
   
   class x {
   	// fluent interface : $this is chainable
   	function foo() {
   		return $this;
   	}
   
   	// Not for fluent interface : the method may return something else
   	function goo($a) {
   		if ($a == true) {
   			return $this;
   		} else {
   			return 3;
   		}
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_
  + `Fluent Interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/fluent-interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/HasNotFluentInterface                                                                                         |
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


