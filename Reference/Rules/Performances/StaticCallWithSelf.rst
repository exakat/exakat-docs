.. _performances-staticcallwithself:


.. _static-call-with-self:

Static Call With Self
+++++++++++++++++++++

.. meta::
	:description:
		Static Call With Self: Avoid using a static call on a non-static method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Call With Self
	:twitter:description: Static Call With Self: Avoid using a static call on a non-static method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Call With Self
	:og:type: article
	:og:description: Avoid using a static call on a non-static method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Call With Self.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/StaticCallWithSelf.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/StaticCallWithSelf.html","name":"Static Call With Self","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Avoid using a static call on a non-static method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Call With Self.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ call on a non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ method. 

PHP allows it inside the class itself. Yet, it makes the code confusing.

.. code-block:: php
   
   <?php
   
   class x {
   	function foo() {
   		self::bar();
   		$this->bar();
   	}
   	
   	// non static method
   	function bar() {
   	
   	}
   }
   
   ?>

See also `Don't call instance methods statically <https://thephp.cc/articles/dont-call-instance-methods-statically>`_.

Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_


Suggestions
___________

* Use the normal method call syntax.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/StaticCallWithSelf                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


