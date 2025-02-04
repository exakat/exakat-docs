.. _functions-wrongargumenttype:


.. _wrong-argument-type:

Wrong Argument Type
+++++++++++++++++++

.. meta::
	:description:
		Wrong Argument Type: Checks that the type of the argument is consistent with the type of the called method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Argument Type
	:twitter:description: Wrong Argument Type: Checks that the type of the argument is consistent with the type of the called method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Argument Type
	:og:type: article
	:og:description: Checks that the type of the argument is consistent with the type of the called method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Argument Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongArgumentType.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongArgumentType.html","name":"Wrong Argument Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Checks that the type of the argument is consistent with the type of the called method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Argument Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Checks that the type of the argument is consistent with the type of the called method.

This analysis is valid since PHP 8.0.

.. code-block:: php
   
   <?php
   
   function foo(int $a) { }
   
   //valid call, with an integer
   foo(1);
   
   //invalid call, with a string
   foo('asd');
   
   ?>
Related PHP errors 
-------------------

  + `Argument #%d ($%s) must be of type %s, %s given <https://php-errors.readthedocs.io/en/latest/messages/argument-%23%25d-%28%24%25s%29-must-be-of-type-%25s%2C-%25s-given.html>`_



Connex PHP features
-------------------

  + `Type System <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `Argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Suggestions
___________

* Always use a valid type when calling methods.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongArgumentType                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.3                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


