.. _functions-multipledeclarations:


.. _multiple-functions-declarations:

Multiple Functions Declarations
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Functions Declarations: Some functions are declared multiple times in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Functions Declarations
	:twitter:description: Multiple Functions Declarations: Some functions are declared multiple times in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Functions Declarations
	:og:type: article
	:og:description: Some functions are declared multiple times in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Functions Declarations.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MultipleDeclarations.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MultipleDeclarations.html","name":"Multiple Functions Declarations","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Some functions are declared multiple times in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Functions Declarations.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some functions are declared multiple times in the code. 

PHP accepts multiple definitions for the same functions, as long as they are not in the same file (linting `error) <https://www.php.net/error>`_, or not included simultaneously during the execution. 

This creates to several situations in which the same functions are defined multiple times : the function may be compatible with various PHP version, but their implementation may not. Or the function is part of a larger library, and sometimes only need without the rest of the library. 

It is recommended to avoid having several functions with the same name in one repository. Turn those functions into methods and load them when needed.

.. code-block:: php
   
   <?php
   
   namespace a {
       function foo() {}
   }
   
   // Other file
   namespace a {
       function foo() {}
       function bar() {}
   }
   
   
   ?>
Connex PHP features
-------------------

  + `declaration <https://php-dictionary.readthedocs.io/en/latest/dictionary/declaration.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MultipleDeclarations                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.0                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


