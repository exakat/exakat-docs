.. _functions-mismatchedtypehint:

.. _mismatched-type:

Mismatched Type
+++++++++++++++

.. meta::
	:description:
		Mismatched Type: Relayed arguments don't have the same type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatched Type
	:twitter:description: Mismatched Type: Relayed arguments don't have the same type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatched Type
	:og:type: article
	:og:description: Relayed arguments don't have the same type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mismatched Type.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MismatchedTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MismatchedTypehint.html","name":"Mismatched Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"Relayed arguments don't have the same type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mismatched Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Relayed arguments don't have the same type.

Type acts as a filter method. When an object is checked with a first class, and then checked again with a second distinct class, the whole process is always false : $a can't be of two different classes at the same time.

Note : This analysis currently doesn't check generalisation of classes : for example, when B is a child of BB, it is still reported as a mismatch.

.. code-block:: php
   
   <?php
   
   // Foo() calls bar()
   function foo(A $a, B $b) {
       bar($a, $b);
   }
   
   // $a is of A typehint in both methods, but 
   // $b is of B then BB typehing
   function bar(A $a, BB $b) {
   
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Ensure that the default value match the expected typehint.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchedTypehint                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.3                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-functions-mismatchedtypehint`                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


