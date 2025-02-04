.. _functions-wrongtypehintedname:


.. _wrong-typed-name:

Wrong Typed Name
++++++++++++++++

.. meta::
	:description:
		Wrong Typed Name: The parameter name doesn't reflect the type used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Typed Name
	:twitter:description: Wrong Typed Name: The parameter name doesn't reflect the type used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Typed Name
	:og:type: article
	:og:description: The parameter name doesn't reflect the type used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Typed Name.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongTypehintedName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongTypehintedName.html","name":"Wrong Typed Name","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"The parameter name doesn't reflect the type used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Typed Name.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The parameter name doesn't reflect the type used.

There are no restriction on parameter names, except its uniqueness in the signature. Yet, using a scalar type as the name for another typed value is just misleading. 

This analysis relies on exact names : calling an array a list of ``string`` is OK with this analysis.

This analysis relies on a few variations of names : ``bool`` and ``boolean``, ``int`` and ``integer``.

.. code-block:: php
   
   <?php
   
   function foo(string $array,
                int $int) {
       // doSomething()
   }
   
   function bar(array $strings) {
       // doSomething()
   }
   
   ?>
Connex PHP features
-------------------

  + `Type System <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Rename the parameter




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongTypehintedName                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


