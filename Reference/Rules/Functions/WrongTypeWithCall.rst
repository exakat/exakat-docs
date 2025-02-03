.. _functions-wrongtypewithcall:


.. _wrong-type-with-call:

Wrong Type With Call
++++++++++++++++++++


.. meta::

	:description:

		Wrong Type With Call: This analysis checks that a call to a method uses the types.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Wrong Type With Call

	:twitter:description: Wrong Type With Call: This analysis checks that a call to a method uses the types

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Wrong Type With Call

	:og:type: article

	:og:description: This analysis checks that a call to a method uses the types

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Type With Call.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongTypeWithCall.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongTypeWithCall.html","name":"Wrong Type With Call","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This analysis checks that a call to a method uses the types","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Type With Call.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis checks that a call to a method uses the types.

This analysis is compatible with Union types and with Intersection types.
Currently, this analysis doesn't take into account ``strict_types = 1``. As such, ``int`` and ``string`` won't be compatible.

.. code-block:: php
   
   <?php
   
   function foo(string $a) {
   
   }
   
   // wrong type used
   foo(1);
   
   // wrong type used
   foo("1");
   
   ?>
Related PHP errors 
-------------------

  + `Argument #1 ($s) must be of type X, int given <https://php-errors.readthedocs.io/en/latest/messages/argument-%23%25d-%28%24%25s%29-must-be-of-type-%25s%2C-%25s-given.html>`_



Connex PHP features
-------------------

  + `union-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/union-type.ini.html>`_
  + `intersection-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/intersection-type.ini.html>`_


Suggestions
___________

* Use the right type with all arguments
* Force the type with a cast
* Check the type before calling




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongTypeWithCall                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


