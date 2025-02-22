.. _functions-fallbackfunction:


.. _fallback-function:

Fallback Function
+++++++++++++++++

.. meta::
	:description:
		Fallback Function: This rule reports functions that are called with its name alone, and whose definition is in the global scope.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Fallback Function
	:twitter:description: Fallback Function: This rule reports functions that are called with its name alone, and whose definition is in the global scope
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Fallback Function
	:og:type: article
	:og:description: This rule reports functions that are called with its name alone, and whose definition is in the global scope
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Fallback Function.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/FallbackFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/FallbackFunction.html","name":"Fallback Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule reports functions that are called with its name alone, and whose definition is in the global scope","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Fallback Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports functions that are called with its name alone, and whose definition is in the global scope. Such syntax relies on the fallback mechanism of PHP, which search for functions in the local namespace, then in the global namespace, before failing.

.. code-block:: php
   
   <?php
   
   namespace {
       // global definition
       function foo() {}
   }
   
   namespace Bar {
       // local definition
       function foo2() {}
       
       foo(); // definition is in the global namespace
       foo2(); // definition is in the Bar namespace
   }
   
   ?>

See also `Using namespaces: fallback to global function/constant <https://www.php.net/manual/en/language.namespaces.fallback.php>`_.

Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `Fallback Function <https://php-dictionary.readthedocs.io/en/latest/dictionary/fallback-function.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/FallbackFunction                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                                                                                   |
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


