.. _security-incompatibletypeswithincoming:


.. _incompatible-types-with-incoming-values:

Incompatible Types With Incoming Values
+++++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Incompatible Types With Incoming Values: This analysis report invalid type used when extracting data from an HTTP request, and using them with typed method.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Incompatible Types With Incoming Values

	:twitter:description: Incompatible Types With Incoming Values: This analysis report invalid type used when extracting data from an HTTP request, and using them with typed method

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Incompatible Types With Incoming Values

	:og:type: article

	:og:description: This analysis report invalid type used when extracting data from an HTTP request, and using them with typed method

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incompatible Types With Incoming Values.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/IncompatibleTypesWithIncoming.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/IncompatibleTypesWithIncoming.html","name":"Incompatible Types With Incoming Values","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis report invalid type used when extracting data from an HTTP request, and using them with typed method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Incompatible Types With Incoming Values.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis report invalid type used when extracting data from an HTTP request, and using them with typed method. 

This currently is based on \symfony\component\httpfoundation\request class, and its related `get*()` methods. 

The analysis also checks usage of superglobals and their related types.

.. code-block:: php
   
   <?php
   
   function foo(\Symfony\Component\HttpFoundation\Request $request) {
   	// This is valid and typed
   	$object = new X($request->getInt('value')); 
   
   	// This is wrong : value is a string, or even an array
   	$object = new X($request->get('value')); 
   }
   
   class X { 
   	function __construct(int $a) {}
   }
   
   foo($_GET['a']);
   // This is missing null type
   function foo(array|string $arg) {}
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Add restriction before calling the methods
* Add possible types in the method definition




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/IncompatibleTypesWithIncoming                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


