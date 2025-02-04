.. _php-globalwithoutsimplevariable:


.. _simple-global-variable:

Simple Global Variable
++++++++++++++++++++++

.. meta::
	:description:
		Simple Global Variable: The global keyword should only be used with simple variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Simple Global Variable
	:twitter:description: Simple Global Variable: The global keyword should only be used with simple variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Simple Global Variable
	:og:type: article
	:og:description: The global keyword should only be used with simple variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Simple Global Variable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/GlobalWithoutSimpleVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/GlobalWithoutSimpleVariable.html","name":"Simple Global Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"The global keyword should only be used with simple variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Simple Global Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The global keyword should only be used with simple variables. Since PHP 7, it cannot be used with complex or dynamic structures.

.. code-block:: php
   
   <?php
   
   // Forbidden in PHP 7
   global $normalGlobal;
   
   // Forbidden in PHP 7
   global $$variable->global ;
   
   // Tolerated in PHP 7
   global $\{$variable->global\}; 
   
   ?>

See also `Changes to the handling of indirect variables, properties, and methods <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.variable-handling.indirect>`_.

Connex PHP features
-------------------

  + `global Scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Suggestions
___________

* Add curly braces so the syntax is compatibles PHP 5 and PHP 7
* Remove this syntax, and access the variable through another way : argument, array, property.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/GlobalWithoutSimpleVariable                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Critical                                                                                                                             |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.6 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/globalDynamicVariable.html>`__                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


