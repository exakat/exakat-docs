.. _classes-propertydefinition:

.. _property-names:

Property Names
++++++++++++++

.. meta::
	:description:
		Property Names: Variables are used in property definitions, when they are located in a class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Names
	:twitter:description: Property Names: Variables are used in property definitions, when they are located in a class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Names
	:og:type: article
	:og:description: Variables are used in property definitions, when they are located in a class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Names.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyDefinition.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyDefinition.html","name":"Property Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Variables are used in property definitions, when they are located in a class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Property Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Variables are used in property definitions, when they are located in a class.

.. code-block:: php
   
   <?php
   
   static $x; // not a property, a static variable
   
   class foo {
       static $x; // now, this is a static property
       public $y, $z = 1; // normal properties
       
       public function bar() {
           static $x; // again, a static variable
       }
   }
   
   ?>

See also `Properties <https://www.php.net/manual/en/language.oop5.properties.php>`_.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyDefinition                                                                                              |
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


