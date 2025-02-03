.. _typehints-missingtypehints:


.. _missing-type-in-definition:

Missing Type In Definition
++++++++++++++++++++++++++

.. meta::
	:description:
		Missing Type In Definition: This rule reports any missing typehints, on parameters, return value, property or class constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Type In Definition
	:twitter:description: Missing Type In Definition: This rule reports any missing typehints, on parameters, return value, property or class constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Type In Definition
	:og:type: article
	:og:description: This rule reports any missing typehints, on parameters, return value, property or class constants
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Type In Definition.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/MissingTypehints.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/MissingTypehints.html","name":"Missing Type In Definition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule reports any missing typehints, on parameters, return value, property or class constants","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Missing Type In Definition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports any missing typehints, on parameters, return value, property or class constants. It is recommended to add types to all possible structures to make the type system more efficient.

`__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ and `__destruct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ should not use typehints, and are omitted.

Class constants are typed starting with PHP 8.3


.. code-block:: php
   
   <?php
   
   // No type on return type
   // n type on parameter 
   function missing($parameter) { 
       /// code
   }
   
   ?>
Connex PHP features
-------------------

  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_
  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_
  + `return-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-value.ini.html>`_


Suggestions
___________

* Add a useful typehint
* Add the mixed typehint




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/MissingTypehints                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


