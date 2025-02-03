.. _structures-shouldmaketernary:

.. _should-use-ternary-operator:

Should Use Ternary Operator
+++++++++++++++++++++++++++

.. meta::
	:description:
		Should Use Ternary Operator: Ternary operators are the best when assigning values to a variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Ternary Operator
	:twitter:description: Should Use Ternary Operator: Ternary operators are the best when assigning values to a variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Ternary Operator
	:og:type: article
	:og:description: Ternary operators are the best when assigning values to a variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Ternary Operator.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldMakeTernary.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldMakeTernary.html","name":"Should Use Ternary Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Ternary operators are the best when assigning values to a variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Ternary Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Ternary operators are the best when assigning values to a variable.

They are less verbose, compatible with assignation and easier to read.

.. code-block:: php
   
   <?php
       // verbose if then structure
       if ($a == 3) {
           $b = 2;
       } else {
           $b = 3;
       }
   
       // compact ternary call
       $b = ($a == 3) ? 2 : 3;
   
       // verbose if then structure
       // Works with short assignations and simple expressions
       if ($a != 3) {
           $b += 2 - $a * 4;
       } else {
           $b += 3;
       }
   
       // compact ternary call
       $b += ($a != 3) ? 2 - $a * 4 : 3;
   
   ?>

See also `Ternary Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.ternary>`_ and `Shorthand comparisons in PHP <https://stitcher.io/blog/shorthand-comparisons-in-php>`_.

Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_


Suggestions
___________

* Use the ternary operator




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldMakeTernary                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-structures-shouldmaketernary`                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


