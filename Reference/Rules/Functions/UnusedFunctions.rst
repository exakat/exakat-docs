.. _functions-unusedfunctions:


.. _unused-functions:

Unused Functions
++++++++++++++++

.. meta::
	:description:
		Unused Functions: The functions below are unused.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Functions
	:twitter:description: Unused Functions: The functions below are unused
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Functions
	:og:type: article
	:og:description: The functions below are unused
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedFunctions.html","name":"Unused Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The functions below are unused","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The functions below are unused. They look like dead code.

Recursive functions, level 1, are detected : they are only reported when a call from outside the function is made. Recursive functions calls of higher level (A calls B calls A) are not handled.

.. code-block:: php
   
   <?php
   
   function used() {}
   // The 'unused' function is defined but never called
   function unused() {}
   
   // The 'used' function is called at least once
   used();
   
   ?>
Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `Unused <https://php-dictionary.readthedocs.io/en/latest/dictionary/unused.ini.html>`_


Suggestions
___________

* Use the function in the code
* Remove the functions from the code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnusedFunctions                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-functions-unusedfunctions`, :ref:`case-piwigo-functions-unusedfunctions`                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


