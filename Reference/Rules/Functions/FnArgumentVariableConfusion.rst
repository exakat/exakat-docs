.. _functions-fnargumentvariableconfusion:


.. _fn-argument-variable-confusion:

Fn Argument Variable Confusion
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Fn Argument Variable Confusion: Avoid using local variables as arrow function arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Fn Argument Variable Confusion
	:twitter:description: Fn Argument Variable Confusion: Avoid using local variables as arrow function arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Fn Argument Variable Confusion
	:og:type: article
	:og:description: Avoid using local variables as arrow function arguments
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Fn Argument Variable Confusion.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/FnArgumentVariableConfusion.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/FnArgumentVariableConfusion.html","name":"Fn Argument Variable Confusion","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using local variables as arrow function arguments","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Fn Argument Variable Confusion.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using local variables as arrow function arguments.

When a local variable name is used as an argument's name in an arrow function, the local variable from the original scope is not imported. They are now two distinct variables.

When the local variable is not listed as argument, it is then imported in the arrow function.

.. code-block:: php
   
   <?php
   
   function foo() {
       $locale = 1;
   
       // Actually ignores the argument, and returns the local variable ``$locale``.
       $fn2 = fn ($argument) => $locale;
   
       // Seems similar to above, but returns the incoming argument    
       $fn2 = fn ($locale) => $locale;
   }
   
   ?>

See also `Arrow functions <https://www.php.net/manual/en/functions.arrow.php>`_.

Connex PHP features
-------------------

  + `Arrow Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrow-function.ini.html>`_


Suggestions
___________

* Change the name of the local variable
* Change the name of the argument




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/FnArgumentVariableConfusion                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.0                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


