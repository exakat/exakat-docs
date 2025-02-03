.. _arrays-floatconversionasindex:


.. _float-conversion-as-index:

Float Conversion As Index
+++++++++++++++++++++++++

.. meta::
	:description:
		Float Conversion As Index: Only integers and strings are possible types when used for array index.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Float Conversion As Index
	:twitter:description: Float Conversion As Index: Only integers and strings are possible types when used for array index
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Float Conversion As Index
	:og:type: article
	:og:description: Only integers and strings are possible types when used for array index
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Float Conversion As Index.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/FloatConversionAsIndex.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/FloatConversionAsIndex.html","name":"Float Conversion As Index","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Only integers and strings are possible types when used for array index","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Float Conversion As Index.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Only integers and strings are possible types when used for array index. Until PHP 8.1, floats were converted to integer by truncation. Since PHP 8.1, a deprecated message is emitted.

 The implicit conversion of float to int which leads to a loss in precision is now deprecated. This affects array keys, int type declarations in coercive mode, and operators working on integers.

.. code-block:: php
   
   <?php
   $a = [];
   $a[15.5]; // deprecated, as key value loses the 0.5 component
   $a[15.0]; // ok, as 15.0 == 15
   ?>

See also `Implicit incompatible float to int conversions <https://www.php.net/manual/en/migration81.deprecated.php#migration81.deprecated.core.implicit-float-conversion>`_.

Related PHP errors 
-------------------

  + `Implicit conversion from float "%s" to int loses precision <https://php-errors.readthedocs.io/en/latest/messages/implicit-conversion-from-float-string-%22%25s%22-to-int-loses.html>`_



Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use the cast operator (string) to convert the floats into strings. The reverse cast is most often possible.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/FloatConversionAsIndex                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


