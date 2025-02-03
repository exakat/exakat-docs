.. _structures-implicitconversiontoint:


.. _implicit-conversion-to-int:

Implicit Conversion To Int
++++++++++++++++++++++++++

.. meta::
	:description:
		Implicit Conversion To Int: PHP warns when a value is implicitely converted from float to int.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Implicit Conversion To Int
	:twitter:description: Implicit Conversion To Int: PHP warns when a value is implicitely converted from float to int
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Implicit Conversion To Int
	:og:type: article
	:og:description: PHP warns when a value is implicitely converted from float to int
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Implicit Conversion To Int.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ImplicitConversionToInt.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ImplicitConversionToInt.html","name":"Implicit Conversion To Int","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"PHP warns when a value is implicitely converted from float to int","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Implicit Conversion To Int.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP warns when a value is implicitely converted from float to int. This usually leads to a loss of precision and unexpected values.

The conversion happens in various situations in PHP lifecycle (extracted from the wiki article): 

+ Bitwise OR operator |
+ Bitwise AND operator &
+ Bitwise XOR operator ^
+ Shift right and left operators
+ Modulo operator
+ The combined assignment operators of the above operators
+ Assignment to a typed property of type int in coercive typing mode
+ Argument for a parameter of type int for both internal and custom functions in coercive typing mode
+ Returning such a value for custom functions declared with a return type of int in coercive typing mode
+ Bitwise NOT operator ~
+ As an array key

This feature is applied to PHP 8.1 and later, yet it is also applicable to older versions of PHP.

.. code-block:: php
   
   <?php
   
   function foo(int $i) {}
   
   //Implicit conversion from float 1.2 to int loses precision
   foo(1.2);
   
   ?>

See also `PHP RFC: Deprecate implicit non-integer-compatible float to int conversions <https://wiki.php.net/rfc/implicit-float-int-deprecate>`_.

Related PHP errors 
-------------------

  + `Implicit conversion from float 1.2 to int loses precision <https://php-errors.readthedocs.io/en/latest/messages/implicit-conversion-from-float-string-%22%25s%22-to-int-loses.html>`_



Connex PHP features
-------------------

  + `type-juggling <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-juggling.ini.html>`_


Suggestions
___________

* Add an explicit cast `(int)` operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ImplicitConversionToInt                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


