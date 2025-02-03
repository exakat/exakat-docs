.. _php-logicalinletters:


.. _logical-should-use-symbolic-operators:

Logical Should Use Symbolic Operators
+++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Logical Should Use Symbolic Operators: Logical operators come in two flavors :  and / &&, || / or, ^ / xor.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Logical Should Use Symbolic Operators

	:twitter:description: Logical Should Use Symbolic Operators: Logical operators come in two flavors :  and / &&, || / or, ^ / xor

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Logical Should Use Symbolic Operators

	:og:type: article

	:og:description: Logical operators come in two flavors :  and / &&, || / or, ^ / xor

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Logical Should Use Symbolic Operators.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/LogicalInLetters.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/LogicalInLetters.html","name":"Logical Should Use Symbolic Operators","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"Logical operators come in two flavors :  and \/ &&, || \/ or, ^ \/ xor","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Logical Should Use Symbolic Operators.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Logical operators come in two flavors :  and / &&, || / or, ^ / xor. However, they are not exchangeable, as && and and have different precedence. 

It is recommended to use the symbol operators, rather than the letter ones.

.. code-block:: php
   
   <?php
   
   // Avoid lettered operator, as they have lower priority than expected
   $a = $b and $c;
   // $a === 3 because equivalent to ($a = $b) and $c;
   
   // safe way to write the above : 
   $a = ($b and $c);
   
   $a = $b && $c;
   // $a === 1
   
   ?>

See also `Logical Operators <https://www.php.net/manual/en/language.operators.logical.php>`_.

Connex PHP features
-------------------

  + `logical <https://php-dictionary.readthedocs.io/en/latest/dictionary/logical.ini.html>`_


Suggestions
___________

* Change the letter operators to the symbol one : and => &&, or => ||, xor => ^. Review the new expressions as processing order may have changed.
* Add parenthesis to make sure that the order is the expected one




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/LogicalInLetters                                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-letter-logical <https://github.com/dseguy/clearPHP/tree/master/rules/no-letter-logical.md>`__                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-cleverstyle-php-logicalinletters`, :ref:`case-openconf-php-logicalinletters`                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


