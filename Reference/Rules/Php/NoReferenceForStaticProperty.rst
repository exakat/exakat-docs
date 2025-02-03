.. _php-noreferenceforstaticproperty:

.. _no-reference-for-static-property:

No Reference For Static Property
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Reference For Static Property: Static properties used to behave independently when set to a reference value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Reference For Static Property
	:twitter:description: No Reference For Static Property: Static properties used to behave independently when set to a reference value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Reference For Static Property
	:og:type: article
	:og:description: Static properties used to behave independently when set to a reference value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Reference For Static Property.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoReferenceForStaticProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoReferenceForStaticProperty.html","name":"No Reference For Static Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"Static properties used to behave independently when set to a reference value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Reference For Static Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties used to behave independently when set to a reference value. This was fixed in PHP 7.3. 

According to the PHP 7.3 changelog : 

In PHP, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties are shared between inheriting classes, unless the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property is explicitly overridden in a child class. However, due to an implementation artifact it was possible to separate the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties by assigning a reference. This loophole has been fixed.

.. code-block:: php
   
   <?php
   
       class Test {
           public static $x = 0;
       }
       class Test2 extends Test { }
       
       Test2::$x = &$x;
       $x = 1;
       
       var_dump(Test::$x, Test2::$x);
       // Previously: int(0), int(1)
       // Now: int(1), int(1)
   
   ?>

See also `PHP 7.3 UPGRADE NOTES <https://github.com/php/php-src/blob/3b6e1ee4ee05678b5d717cd926a35ffdc1335929/UPGRADING#L66-L81>`_.

Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_
  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/NoReferenceForStaticProperty                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.4.9                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.3 and older                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.3 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/staticWithReference.html>`__                                                                                                                                                                                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


