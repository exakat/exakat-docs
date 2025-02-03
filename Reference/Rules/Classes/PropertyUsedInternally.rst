.. _classes-propertyusedinternally:


.. _internally-used-properties:

Internally Used Properties
++++++++++++++++++++++++++

.. meta::
	:description:
		Internally Used Properties: Properties that are used internally.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Internally Used Properties
	:twitter:description: Internally Used Properties: Properties that are used internally
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Internally Used Properties
	:og:type: article
	:og:description: Properties that are used internally
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Internally Used Properties.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyUsedInternally.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyUsedInternally.html","name":"Internally Used Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Properties that are used internally","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Internally Used Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Properties that are used internally.

.. code-block:: php
   
   <?php
   
   class x {
       public $internallyUsedProperty = 1;
       public $externallyUsedProperty = 1;
       public $alsoExternallyUsedProperty = 1;
       
       function foo() {
           $this->internallyUsedProperty = 2;
       }
   }
   
   class y extends x {
       function bar() {
           $this->externallyUsedProperty = 3;
       }
   }
   
   $X = new x();
   $X->alsoExternallyUsedProperty = 3;
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedInternally                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


