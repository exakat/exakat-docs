.. _classes-constructor:


.. _constructors:

Constructors
++++++++++++

.. meta::
	:description:
		Constructors: This rule marks methods as constructors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constructors
	:twitter:description: Constructors: This rule marks methods as constructors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constructors
	:og:type: article
	:og:description: This rule marks methods as constructors
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constructors.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/Constructor.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/Constructor.html","name":"Constructors","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule marks methods as constructors","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Constructors.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule marks methods as constructors. In PHP 8.0 and more recent, only the magic method ``__construct`` is the constructor. In older versions, the method with the same name than the class was the constructor, although with a lower priority than the magic method.

.. code-block:: php
   
   <?php
   
   class x {
       // Normal constructor
       function __construct() {}
   }
   
   class y {
       // Old style constructor, obsolete since PHP 7.1
       function y() {}
   }
   
   class z {
       // Normal constructor
       function __construct() {}
   
       // Old style constructor, but with lower priority
       function z() {}
   }
   
   ?>

See also `Constructors and Destructors <https://www.php.net/manual/en/language.oop5.decon.php>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/Constructor                                                                                                     |
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


