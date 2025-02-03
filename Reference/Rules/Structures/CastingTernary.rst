.. _structures-castingternary:


.. _casting-ternary:

Casting Ternary
+++++++++++++++

.. meta::
	:description:
		Casting Ternary: Type casting has a precedence over ternary operator, and is applied first.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Casting Ternary
	:twitter:description: Casting Ternary: Type casting has a precedence over ternary operator, and is applied first
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Casting Ternary
	:og:type: article
	:og:description: Type casting has a precedence over ternary operator, and is applied first
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Casting Ternary.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CastingTernary.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CastingTernary.html","name":"Casting Ternary","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"Type casting has a precedence over ternary operator, and is applied first","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Casting Ternary.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Type casting has a precedence over ternary operator, and is applied first. When this happens, the condition is cast, although it is often useless as PHP will do it if needed.

This applies to the ternary operator, the coalesce operator ?: and the null-coalesce operator ??.
The last example generates first an `error <https://www.php.net/error>`_ `Undefined variable: b`, since $b is first cast to a string. The `result <https://www.php.net/result>`_ is then an empty string, which leads to an empty string to be stored into $a. Multiple errors cascade.

.. code-block:: php
   
   <?php
       $a = (string) $b ? 3 : 4;
       $a = (string) $b ?: 4;
       $a = (string) $b ?? 4;
   ?>

See also `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Related PHP errors 
-------------------

  + `Undefined variable: <https://php-errors.readthedocs.io/en/latest/messages/undefined-variable.html>`_



Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_
  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Add parenthesis around the ternary operator
* Skip the casting
* Cast in another expression




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CastingTernary                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


