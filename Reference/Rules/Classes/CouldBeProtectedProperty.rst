.. _classes-couldbeprotectedproperty:


.. _could-be-protected-property:

Could Be Protected Property
+++++++++++++++++++++++++++

.. meta::
	:description:
		Could Be Protected Property: Those properties are declared public, but are never used publicly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Protected Property
	:twitter:description: Could Be Protected Property: Those properties are declared public, but are never used publicly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Protected Property
	:og:type: article
	:og:description: Those properties are declared public, but are never used publicly
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Protected Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeProtectedProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeProtectedProperty.html","name":"Could Be Protected Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those properties are declared public, but are never used publicly","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Protected Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those properties are declared public, but are never used publicly. They may be made protected. 

This property may even be made private.

.. code-block:: php
   
   <?php
   
   class foo {
       // Public, and used publicly
       public $publicProperty;
       // Public, but never used outside the class or its children
       public $protectedProperty;
       
       function bar() {
           $this->protectedProperty = 1;
       }
   }
   
   $foo = new Foo();
   $foo->publicProperty = 3;
   
   ?>
Connex PHP features
-------------------

  + `Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Use protected visibility with these properties.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeProtectedProperty                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.7                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


