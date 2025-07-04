.. _variables-staticvariableinitialisation:


.. _static-variable-initialisation:

Static Variable Initialisation
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Static Variable Initialisation: Static variables can be initialized like any other variable, straight from the ``static`` keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Variable Initialisation
	:twitter:description: Static Variable Initialisation: Static variables can be initialized like any other variable, straight from the ``static`` keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Variable Initialisation
	:og:type: article
	:og:description: Static variables can be initialized like any other variable, straight from the ``static`` keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Variable Initialisation.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/StaticVariableInitialisation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/StaticVariableInitialisation.html","name":"Static Variable Initialisation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Static variables can be initialized like any other variable, straight from the ``static`` keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Variable Initialisation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables can be initialized like any other variable, straight from the ``static`` keyword. This was added in PHP 8.3.

Indeed, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are variables, so they shall be initialized with any value, another variable or a functioncall. This behavior is different from the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ constant expression, where only a small set of operators and constants can be used.

.. code-block:: php
   
   <?php
   
   function foo(int $a = 0) {
   	static $s = 1;
   
   	static $s2 = $a + 1;
   }
   ?>
Connex PHP features
-------------------

  + `Constant Scalar Expression <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-constant-expression.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/StaticVariableInitialisation                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


