.. _type-similarintegers:


.. _similar-integers:

Similar Integers
++++++++++++++++

.. meta::
	:description:
		Similar Integers: This analysis reports all integer values that are expressed in different format.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Similar Integers
	:twitter:description: Similar Integers: This analysis reports all integer values that are expressed in different format
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Similar Integers
	:og:type: article
	:og:description: This analysis reports all integer values that are expressed in different format
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Similar Integers.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/SimilarIntegers.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/SimilarIntegers.html","name":"Similar Integers","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis reports all integer values that are expressed in different format","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Similar Integers.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis reports all integer values that are expressed in different format.

.. code-block:: php
   
   <?php
   
   // Three ways to write 10 (more available)
   $a = 10;
   $b = 012;
   $x = 0xA;
   
   // 7 is expressed in one way only
   $d = 7;
   $d = 7;
   
   // Four ways to write 11 (more available)
   $a = 11;
   $b = 013;
   $x = 0xB;
   $x = -+-11;
   
   // Expressions are not counted
   
   ?>
Connex PHP features
-------------------

  + `integer <https://php-dictionary.readthedocs.io/en/latest/dictionary/integer.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/SimilarIntegers                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


