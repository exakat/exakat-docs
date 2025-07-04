.. _traits-cannotcalltraitstaticproperty:


.. _cannot-call-trait-static-property:

Cannot Call Trait Static Property
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Cannot Call Trait Static Property: It is deprecated to use a static trait property directly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cannot Call Trait Static Property
	:twitter:description: Cannot Call Trait Static Property: It is deprecated to use a static trait property directly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cannot Call Trait Static Property
	:og:type: article
	:og:description: It is deprecated to use a static trait property directly
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cannot Call Trait Static Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/CannotCallTraitStaticProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/CannotCallTraitStaticProperty.html","name":"Cannot Call Trait Static Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 06 May 2025 05:11:57 +0000","dateModified":"Tue, 06 May 2025 05:11:57 +0000","description":"It is deprecated to use a static trait property directly","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cannot Call Trait Static Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is deprecated to use a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ trait property directly. It should be used within its host class, and not independently.

.. code-block:: php
   
   <?php
   
   trait T {
   	public static $property = 1;
   }
   
   echo T::$property;
   T::$property = 2;
   
   ?>
Connex PHP features
-------------------

  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `Properties <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Use the trait in a class, and use that class instead of the trait.




Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Traits/CannotCallTraitStaticProperty                             |
+--------------+------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+------------------------------------------------------------------+
| Exakat since | 2.7.2                                                            |
+--------------+------------------------------------------------------------------+
| PHP Version  | With PHP 9.0 and older                                           |
+--------------+------------------------------------------------------------------+
| Severity     | Minor                                                            |
+--------------+------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                  |
+--------------+------------------------------------------------------------------+
| Precision    | High                                                             |
+--------------+------------------------------------------------------------------+
| Available in |                                                                  |
+--------------+------------------------------------------------------------------+


