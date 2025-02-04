.. _classes-constvisibilityusage:


.. _const-visibility-usage:

Const Visibility Usage
++++++++++++++++++++++

.. meta::
	:description:
		Const Visibility Usage: Visibility for class constant controls the accessibility to class constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Const Visibility Usage
	:twitter:description: Const Visibility Usage: Visibility for class constant controls the accessibility to class constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Const Visibility Usage
	:og:type: article
	:og:description: Visibility for class constant controls the accessibility to class constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Const Visibility Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ConstVisibilityUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ConstVisibilityUsage.html","name":"Const Visibility Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Visibility for class constant controls the accessibility to class constant","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Const Visibility Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Visibility for class constant controls the accessibility to class constant.

A public constant may be used anywhere in the code; a protected constant usage is restricted to the class and its relatives; a private constant is restricted to itself.

This feature was introduced in PHP 7.1. It is recommended to use explicit visibility, and, whenever possible, make the visibility private.

.. code-block:: php
   
   <?php
   
   class x {
       public const a = 1;
       protected const b = 2;
       private const c = 3;
       const d = 4;
   }
   
   interface i {
       public const a = 1;
         const d = 4;
   }
   
   ?>

See also `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_ and `PHP RFC: Support Class Constant Visibility <https://wiki.php.net/rfc/class_const_visibility>`_.

Connex PHP features
-------------------

  + `Class Constants Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant-visibility.ini.html>`_


Suggestions
___________

* Add constant visibility, at least 'public'.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ConstVisibilityUsage                                                                                                                                                                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                                                                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and more recent                                                                                                                                                                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


