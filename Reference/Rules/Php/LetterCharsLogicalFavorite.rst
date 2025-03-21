.. _php-lettercharslogicalfavorite:


.. _logical-operators-favorite:

Logical Operators Favorite
++++++++++++++++++++++++++

.. meta::
	:description:
		Logical Operators Favorite: PHP has two sets of logical operators : letters (and, or, xor) and chars (&&, ||, ^).
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Logical Operators Favorite
	:twitter:description: Logical Operators Favorite: PHP has two sets of logical operators : letters (and, or, xor) and chars (&&, ||, ^)
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Logical Operators Favorite
	:og:type: article
	:og:description: PHP has two sets of logical operators : letters (and, or, xor) and chars (&&, ||, ^)
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Logical Operators Favorite.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/LetterCharsLogicalFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/LetterCharsLogicalFavorite.html","name":"Logical Operators Favorite","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP has two sets of logical operators : letters (and, or, xor) and chars (&&, ||, ^)","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Logical Operators Favorite.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP has two sets of logical operators : letters (and, or, xor) and chars (&&, ||, ^). 

The analyzed code has less than 10% of one of the two sets : for consistency reasons, it is recommended to make them all the same. 

Warning : the two sets of operators have different precedence levels. Using and or && is not exactly the same, especially and not only, when assigning the results to a variable. 
Using and or && are also the target of other analysis.

.. code-block:: php
   
   <?php 
   
   $a1 = $b and $c;
   $a1 = $b and $c;
   $a1 = $b and $c;
   $a1 = $b or $c;
   $a1 = $b OR $c;
   $a1 = $b and $c;
   $a1 = $b and $c;
   $a1 = $b and $c;
   $a1 = $b or $c;
   $a1 = $b OR $c;
   $a1 = $b ^ $c;
   
   ?>

See also `Logical Operators <https://www.php.net/manual/en/language.operators.logical.php>`_ and `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `Logical Operators <https://php-dictionary.readthedocs.io/en/latest/dictionary/logical-operator.ini.html>`_


Suggestions
___________

* Pick a favorite, and enforce it




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/LetterCharsLogicalFavorite                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


