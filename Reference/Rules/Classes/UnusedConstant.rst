.. _classes-unusedconstant:

.. _unused-class-constant:

Unused Class Constant
+++++++++++++++++++++

.. meta::
	:description:
		Unused Class Constant: The class constant is unused.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Class Constant
	:twitter:description: Unused Class Constant: The class constant is unused
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Class Constant
	:og:type: article
	:og:description: The class constant is unused
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Class Constant.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnusedConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnusedConstant.html","name":"Unused Class Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The class constant is unused","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Class Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The class constant is unused. Consider removing it or using it.

Class constants may be used in expressions, in `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expressions, when building other constants, or in default values.

.. code-block:: php
   
   <?php
   
   class foo {
       public const UNUSED = 1; // No mention in the code
       
       private const USED = 2;  // used constant
       
       function bar() {
           echo self::USED;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Suggestions
___________

* Remove the class constant
* Use the class constant




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedConstant                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


