.. _php-onlyvariablepassedbyreference:


.. _only-variable-passed-by-reference:

Only Variable Passed By Reference
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Only Variable Passed By Reference: Some methods require a variable as argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Only Variable Passed By Reference
	:twitter:description: Only Variable Passed By Reference: Some methods require a variable as argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Only Variable Passed By Reference
	:og:type: article
	:og:description: Some methods require a variable as argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Only Variable Passed By Reference.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/OnlyVariablePassedByReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/OnlyVariablePassedByReference.html","name":"Only Variable Passed By Reference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Some methods require a variable as argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Only Variable Passed By Reference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some methods require a variable as argument. Those arguments are passed by reference, and they must operate on a variable, or any data container (property, array element). 

This means that literal values, constants cannot be used as argument. This is also the case of literal values, returned by other methods.

This is also the case of ``isset()``, althought with a different `error <https://www.php.net/error>`_ message.

.. code-block:: php
   
   <?php
   
   echo end([1,2,3]);
   
   function foo() {
   	return [4,5,6];
   }
   
   echo end(foo());
   
   ?>
Related PHP errors 
-------------------

  + `Argument #1 ($array) could not be passed by reference <https://php-errors.readthedocs.io/en/latest/messages/%25s%28%29%3A-argument-%23%25d%25s%25s%25s-could-not-be-passed-by-reference.html>`_
  + `Argument #1 ($array) cannot be passed by reference <https://php-errors.readthedocs.io/en/latest/messages/%25s%28%29-argument-%23%25d%25s%25s%25s-cannot-be-passed-by-reference.html>`_
  + `Cannot use isset() on the result of an expression (you can use "null !== expression" instead) <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-isset%28%29-on-the-result-of-an-expression-%28you-can-use-%22null-%21%3D%3D-expression%22-instead%29.html>`_




Suggestions
___________

* Put the value in a variable before using it with the function.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/OnlyVariablePassedByReference                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


