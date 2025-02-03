.. _classes-locallyunusedproperty:

.. _locally-unused-property:

Locally Unused Property
+++++++++++++++++++++++

.. meta::
	:description:
		Locally Unused Property: Those properties are defined in a class, and this class doesn't have any method that makes use of them.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Locally Unused Property
	:twitter:description: Locally Unused Property: Those properties are defined in a class, and this class doesn't have any method that makes use of them
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Locally Unused Property
	:og:type: article
	:og:description: Those properties are defined in a class, and this class doesn't have any method that makes use of them
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Locally Unused Property.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/LocallyUnusedProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/LocallyUnusedProperty.html","name":"Locally Unused Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those properties are defined in a class, and this class doesn't have any method that makes use of them","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Locally Unused Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those properties are defined in a class, and this class doesn't have any method that makes use of them. 

While this is syntactically correct, it is unusual that defined resources are used in a child class. It may be worth moving the definition to another class, or to move accessing methods to the class.

.. code-block:: php
   
   <?php
   
   class foo {
       public $unused, $used;// property $unused is never used in this class
       
       function bar() {
           $this->used++; // property $used is used in this method
       }
   }
   
   class foofoo extends foo {
       function bar() {
           $this->unused++; // property $unused is used in this method, but defined in the parent class
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Move the property definition to the child classes
* Move some of the child method, using the property, to the parent class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/LocallyUnusedProperty                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


