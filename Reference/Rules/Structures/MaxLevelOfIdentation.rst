.. _structures-maxlevelofidentation:

.. _max-level-of-nesting:

Max Level Of Nesting
++++++++++++++++++++

.. meta::
	:description:
		Max Level Of Nesting: Avoid nesting structures too deep, as it hurts readability.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Max Level Of Nesting
	:twitter:description: Max Level Of Nesting: Avoid nesting structures too deep, as it hurts readability
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Max Level Of Nesting
	:og:type: article
	:og:description: Avoid nesting structures too deep, as it hurts readability
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Max Level Of Nesting.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MaxLevelOfIdentation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MaxLevelOfIdentation.html","name":"Max Level Of Nesting","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Avoid nesting structures too deep, as it hurts readability","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Max Level Of Nesting.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Avoid nesting structures too deep, as it hurts readability.

Nesting structures are : if/then, switch, for, foreach, while, do...while. Ternary operator, try/catch are not considered a nesting structures.

Closures, and more generally, functions definitions are counted separatedly. 

This analysis checks for 4 levels of nesting, by default. This may be changed by configuration.

.. code-block:: php
   
   <?php
   
   // 5 levels of indentation
   function foo() {
       if (1) {
           if (2) {
               if (3) {
                   if (4) {
                       if (5) {
                           51;
                       } else {
                           5;
                       }
                   } else {
                       4;
                   }
               } else {
                   3;
               }
           } else {
               2;
           }
       } else {
           1;
       }
   }
   
   // 2 levels of indentation
   function foo() {
       if (1) {
           if (2) {
               // 3 levels of indentation
               return function () {
                   if (3) {
                       if (4) {
                           if (5) {
                               51;
                           } else {
                               5;
                           }
                       } else {
                           4;
                       }
                   } else {
                       3;
                   }
               }
           } else {
               2;
           }
       } else {
           1;
       }
   }
   
   ?>

+----------+---------+---------+---------------------------------------------------------------------+
| Name     | Default | Type    | Description                                                         |
+----------+---------+---------+---------------------------------------------------------------------+
| maxLevel | 4       | integer | Maximum level of nesting for control flow structures in one scope.  |
+----------+---------+---------+---------------------------------------------------------------------+



See also `Indentation and Spacing in PHP <https://courses.cs.washington.edu/courses/cse154/17au/styleguide/php/spacing-indentation-php.html>`.

Connex PHP features
-------------------

  + `indentation <https://php-dictionary.readthedocs.io/en/latest/dictionary/indentation.ini.html>`_


Suggestions
___________

* Refactor code to avoid nesting
* Export some nested blocks to an external method or function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MaxLevelOfIdentation                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
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


