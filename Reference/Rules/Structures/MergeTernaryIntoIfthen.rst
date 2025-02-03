.. _structures-mergeternaryintoifthen:

.. _could-merge-ternary-into-ifthen:

Could Merge Ternary Into Ifthen
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Could Merge Ternary Into Ifthen: When two ternary operators are used, in succession, with the same condition, it might be more readable to write it as an if then condition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Merge Ternary Into Ifthen
	:twitter:description: Could Merge Ternary Into Ifthen: When two ternary operators are used, in succession, with the same condition, it might be more readable to write it as an if then condition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Merge Ternary Into Ifthen
	:og:type: article
	:og:description: When two ternary operators are used, in succession, with the same condition, it might be more readable to write it as an if then condition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Merge Ternary Into Ifthen.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MergeTernaryIntoIfthen.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MergeTernaryIntoIfthen.html","name":"Could Merge Ternary Into Ifthen","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When two ternary operators are used, in succession, with the same condition, it might be more readable to write it as an if then condition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Merge Ternary Into Ifthen.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When two ternary operators are used, in succession, with the same condition, it might be more readable to write it as an if then condition.

With an if then structure, the related instructions are grouped together, while they are scattered otherwise.

Readability improves with more ternaries in a row.

.. code-block:: php
   
   <?php
   
   $variable1 = $a ? 'b0' : $c;
   $variable2 = $a ? foo() : null;
   
   if ($a) {
   	$variable1 = 'b0';
   	$variable2 = foo();
   } else {
   	$variable1 = $c;
   	$variable2 = null;
   }
   
   ?>
Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MergeTernaryIntoIfthen                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


