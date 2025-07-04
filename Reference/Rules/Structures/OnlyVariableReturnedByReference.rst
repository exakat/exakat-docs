.. _structures-onlyvariablereturnedbyreference:


.. _only-variable-returned-by-reference:

Only Variable Returned By Reference
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Only Variable Returned By Reference: Function can't return literals by reference.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Only Variable Returned By Reference
	:twitter:description: Only Variable Returned By Reference: Function can't return literals by reference
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Only Variable Returned By Reference
	:og:type: article
	:og:description: Function can't return literals by reference
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Only Variable Returned By Reference.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OnlyVariableReturnedByReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OnlyVariableReturnedByReference.html","name":"Only Variable Returned By Reference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Function can't return literals by reference","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Only Variable Returned By Reference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Function can't return literals by reference.

When a function returns a reference, it is only possible to return variables, properties or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties. 

Anything else, like literals or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expressions, yield a warning at execution time.

.. code-block:: php
   
   <?php
   
   // Can't return a literal number
   function &foo() {
       return 3 + rand();
   }
   
   // bar must return values that are stored in a 
   function &bar() {
       $a = 3 + rand();
       return $a;
   }
   
   ?>
Connex PHP features
-------------------

  + `References <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OnlyVariableReturnedByReference                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


