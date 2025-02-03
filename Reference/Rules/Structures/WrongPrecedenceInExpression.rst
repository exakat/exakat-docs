.. _structures-wrongprecedenceinexpression:


.. _wrong-precedence-in-expression:

Wrong Precedence In Expression
++++++++++++++++++++++++++++++


.. meta::

	:description:

		Wrong Precedence In Expression: These operators are not executed in the expected order.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Wrong Precedence In Expression

	:twitter:description: Wrong Precedence In Expression: These operators are not executed in the expected order

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Wrong Precedence In Expression

	:og:type: article

	:og:description: These operators are not executed in the expected order

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Precedence In Expression.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WrongPrecedenceInExpression.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WrongPrecedenceInExpression.html","name":"Wrong Precedence In Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"These operators are not executed in the expected order","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Precedence In Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

These operators are not executed in the expected order. Coalesce and ternary operator have lesser precedence compared to comparisons or spaceship operators. 

Thus, the comparison is executed first, and the other operator later. 

It is recomended to use parenthesis in these cases.

Note that this may behave as expected, with a bit of clever placing boolean: see last example.

.. code-block:: php
   
   <?php
   
   // This 
   if ($a ?? 1 == 2) {} 
   
   // is equivalent to 
   if ($a ?? (1 == 2)) {} 
   
   // It is different from
   if (($a ?? 1) == 2) {} 
   
   // This one is also wrong, but falls back on correct values
   if ($a ?? false === true) {} 
   
   ?>

Suggestions
___________

* Add parenthesis around the coalesce operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/WrongPrecedenceInExpression                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


