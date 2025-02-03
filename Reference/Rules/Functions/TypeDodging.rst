.. _functions-typedodging:

.. _type-dodging:

Type Dodging
++++++++++++

.. meta::
	:description:
		Type Dodging: It is always possible to rewrite a parameter type by using union types.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Type Dodging
	:twitter:description: Type Dodging: It is always possible to rewrite a parameter type by using union types
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Type Dodging
	:og:type: article
	:og:description: It is always possible to rewrite a parameter type by using union types
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Type Dodging.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TypeDodging.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TypeDodging.html","name":"Type Dodging","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is always possible to rewrite a parameter type by using union types","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Type Dodging.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>It is always possible to rewrite a parameter type by using union types. When the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class or interface requires a type, the child class may create a union type with the required type, add a secondary type and ignore the first one. 

This is part of the Liskov Substitution Principle, so the syntax is legit. When the union type is only used to circumvent the previous typing, it is now a violation, as such a typed data would be valid, but ignored.

.. code-block:: php
   
   <?php
   
   interface i {
   	function foo(A $a) {}
   }
   
   class x implement i {
   	function foo(A | string $a) {
   		if ($a instanceof A) {
   			throw new Exception('Unused type.');
   		}
   		// ...
   	}
   } 
   ?>
Connex PHP features
-------------------

  + `liskov <https://php-dictionary.readthedocs.io/en/latest/dictionary/liskov.ini.html>`_


Suggestions
___________

* Avoid using union type to enlarge types in parameters




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TypeDodging                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


