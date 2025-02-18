.. _php-reservedkeywords7:


.. _reserved-keywords-in-php-7:

Reserved Keywords In PHP 7
++++++++++++++++++++++++++

.. meta::
	:description:
		Reserved Keywords In PHP 7: PHP reserved names for class/trait/interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Reserved Keywords In PHP 7
	:twitter:description: Reserved Keywords In PHP 7: PHP reserved names for class/trait/interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Reserved Keywords In PHP 7
	:og:type: article
	:og:description: PHP reserved names for class/trait/interface
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Reserved Keywords In PHP 7.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ReservedKeywords7.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ReservedKeywords7.html","name":"Reserved Keywords In PHP 7","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"PHP reserved names for class\/trait\/interface","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Reserved Keywords In PHP 7.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP reserved names for class/trait/interface. They won't be available anymore in user space starting with PHP 7.

For example, string, float, `false <https://www.php.net/false>`_, `true <https://www.php.net/true>`_, `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, resource,`... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ are not acceptable as class name.

.. code-block:: php
   
   <?php
   
   // This doesn't compile in PHP 7.0 and more recent
   class null { }
   
   ?>

See also `List of other reserved words <https://www.php.net/manual/en/reserved.other-reserved-words.php>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Avoid using PHP reserved keywords as names for structures such as class, trait, interface, enumeration, functions, and global constants. They are still valid for properties, method names and class constants.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ReservedKeywords7                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


