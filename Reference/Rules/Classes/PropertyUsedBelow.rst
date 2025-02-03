.. _classes-propertyusedbelow:


.. _property-used-below:

Property Used Below
+++++++++++++++++++

.. meta::
	:description:
		Property Used Below: This rule marks properties that are used in children classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Used Below
	:twitter:description: Property Used Below: This rule marks properties that are used in children classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Used Below
	:og:type: article
	:og:description: This rule marks properties that are used in children classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Used Below.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyUsedBelow.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyUsedBelow.html","name":"Property Used Below","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule marks properties that are used in children classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Property Used Below.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule marks properties that are used in children classes.

This analysis doesn't mark the current class, nor the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or grand `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes.

.. code-block:: php
   
   <?php
   
   class foo {
       // This property is used in children
       protected protectedProperty = 1;
       
       // This property is not used in children
       protected localProtectedProperty = 1;
   
       private function foobar() {
           // protectedProperty is used here, but defined in parent
           $this->localProtectedProperty = 3;
       }
   }
   
   class foofoo extends foo {
       private function bar() {
           // protectedProperty is used here, but defined in parent
           $this->protectedProperty = 3;
       }
   }
   
   ?>

See also :ref:`Property Used Above <property-used-above>`.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedBelow                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


