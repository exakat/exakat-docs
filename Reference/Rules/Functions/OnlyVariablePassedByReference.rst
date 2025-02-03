.. _functions-onlyvariablepassedbyreference:


.. _only-variable-passed-by-reference:

Only Variable Passed By Reference
+++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Only Variable Passed By Reference: When an argument is expected by reference, it is compulsory to provide a container.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Only Variable Passed By Reference

	:twitter:description: Only Variable Passed By Reference: When an argument is expected by reference, it is compulsory to provide a container

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Only Variable Passed By Reference

	:og:type: article

	:og:description: When an argument is expected by reference, it is compulsory to provide a container

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Only Variable Passed By Reference.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/OnlyVariablePassedByReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/OnlyVariablePassedByReference.html","name":"Only Variable Passed By Reference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"When an argument is expected by reference, it is compulsory to provide a container","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Only Variable Passed By Reference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When an argument is expected by reference, it is compulsory to provide a container. A container may be a variable, an array, a property or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property. 

This may be linted by PHP, when the function definition is in the same file as the function usage. This is silently linted if definition and usage are separated, if the call is dynamical or made as a method.
This analysis currently covers functioncalls and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methodcalls, but omits methodcalls.

.. code-block:: php
   
   <?php
   
   function foo(&$bar) { /**/ }
   
   function &bar() { /**/ }
   
   // This is not possible : strtolower() returns a value
   foo(strtolower($string));
   
   // This is valid : bar() returns a reference
   foo(bar($string));
   
   ?>

See also `Passing arguments by reference <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.by-reference>`_.

Related PHP errors 
-------------------

  + `%s()-Argument #%d ($%s) cannot be passed by reference <https://php-errors.readthedocs.io/en/latest/messages/%25s%28%29%3A-argument-%23%25d%25s%25s%25s-cannot-be-passed-by-reference.html>`_



Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_
  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Store the previous result in a variable, and then call the function.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/OnlyVariablePassedByReference                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-functions-onlyvariablepassedbyreference`, :ref:`case-phpipam-functions-onlyvariablepassedbyreference` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


