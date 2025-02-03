.. _variables-staticvariableinnamespace:


.. _static-variable-in-namespace:

Static Variable In Namespace
++++++++++++++++++++++++++++


.. meta::

	:description:

		Static Variable In Namespace: Static variables may be declared outside a function scope, but it has no usage.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Static Variable In Namespace

	:twitter:description: Static Variable In Namespace: Static variables may be declared outside a function scope, but it has no usage

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Static Variable In Namespace

	:og:type: article

	:og:description: Static variables may be declared outside a function scope, but it has no usage

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Variable In Namespace.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/StaticVariableInNamespace.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/StaticVariableInNamespace.html","name":"Static Variable In Namespace","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Static variables may be declared outside a function scope, but it has no usage","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Variable In Namespace.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables may be declared outside a function scope, but it has no usage. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are persistent between function calls, and there is not such thing as namespace call (including an 'include' call).

.. code-block:: php
   
   <?php
   
   namespace A {
   	// Static has no value here.
   	static $a = 1;
   	
   	function foo() {
   		// One useful static variable
   		static $static = 2;
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `static-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_
  + `namespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_


Suggestions
___________

* Remove the 'static' keyword in the code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/StaticVariableInNamespace                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


