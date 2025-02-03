.. _typehints-couldnottype:

.. _could-not-type:

Could Not Type
++++++++++++++

.. meta::
	:description:
		Could Not Type: Mark arguments, return types and properties that could not be typed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Not Type
	:twitter:description: Could Not Type: Mark arguments, return types and properties that could not be typed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Not Type
	:og:type: article
	:og:description: Mark arguments, return types and properties that could not be typed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Not Type.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldNotType.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldNotType.html","name":"Could Not Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark arguments, return types and properties that could not be typed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Not Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Mark arguments, return types and properties that could not be typed.
Arguments, return types and properties that have no explicit typehint, and that could yield no guess from the following analysis, are deemed unable to receive a type. 

+ `Typehints/CouldBeCIT`
+ `Typehints/CouldBeString`
+ `Typehints/CouldBeArray`
+ `Typehints/CouldBeBoolean`
+ `Typehints/CouldBeVoid`
+ `Typehints/CouldBeCallable`

``mixed`` typehint, which acts as the universal typehint, is not processed here.

There are situation which cannot be typed, and legit : the example below is an illustration. `array_fill() <https://www.php.net/array_fill>`_ is a native PHP example, where the second argument may be of any type. `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_ are also notoriously difficult to type, given the broad usage of arguments.

.. code-block:: php
   
   <?php
   
   // Accepts any input, and returns any input
   // This may be used, but not typed.
   function foo($b) {
       return $b;
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldNotType                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


