.. _classes-definedstaticmp:


.. _defined-static-or-self:

Defined static\:\: Or self\:\:
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Defined static:: Or self::: List of all defined static and self properties and methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Defined static:: Or self::
	:twitter:description: Defined static:: Or self::: List of all defined static and self properties and methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Defined static:: Or self::
	:og:type: article
	:og:description: List of all defined static and self properties and methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Defined static:: Or self::.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DefinedStaticMP.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DefinedStaticMP.html","name":"Defined static:: Or self::","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"List of all defined static and self properties and methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Defined static:: Or self::.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of all defined `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ properties and methods.

.. code-block:: php
   
   <?php
   
   class x {
       static public function definedStatic() {}
       private definedStatic = 1;
       
       public function method() {
           self::definedStatic();
           self::undefinedStatic();
   
           static::definedStatic;
           static::undefinedStatic;
       }
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DefinedStaticMP                                                                                                 |
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


