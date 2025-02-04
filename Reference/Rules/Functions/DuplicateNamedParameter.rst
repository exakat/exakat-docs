.. _functions-duplicatenamedparameter:


.. _duplicate-named-parameter:

Duplicate Named Parameter
+++++++++++++++++++++++++

.. meta::
	:description:
		Duplicate Named Parameter: Two parameters have the same name in a method call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Duplicate Named Parameter
	:twitter:description: Duplicate Named Parameter: Two parameters have the same name in a method call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Duplicate Named Parameter
	:og:type: article
	:og:description: Two parameters have the same name in a method call
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Duplicate Named Parameter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/DuplicateNamedParameter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/DuplicateNamedParameter.html","name":"Duplicate Named Parameter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 04 Feb 2025 11:02:08 +0000","dateModified":"Tue, 04 Feb 2025 11:02:08 +0000","description":"Two parameters have the same name in a method call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Duplicate Named Parameter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Two parameters have the same name in a method call. This yields a Fatal `error <https://www.php.net/error>`_ at execution time.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {}
   
   // parameters are all distinct
   foo(a:1, b:2);
   
   // parameter a is double
   foo(a:1, a:1);
   
   ?>

See also https://www.php.net/manual/en/functions.arguments.php.

Related PHP errors 
-------------------

  + `Named parameter $a overwrites previous argument <https://php-errors.readthedocs.io/en/latest/messages/named-parameter-%24%25s-overwrites-previous-argument.html>`_



Connex PHP features
-------------------

  + `Named Parameters <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Review the parameters names and remove the duplicates
* Review the parameters names and makes the names unique




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DuplicateNamedParameter                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


