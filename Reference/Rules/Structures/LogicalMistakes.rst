.. _structures-logicalmistakes:

.. _logical-mistakes:

Logical Mistakes
++++++++++++++++

.. meta::
	:description:
		Logical Mistakes: Avoid logical mistakes within long expressions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Logical Mistakes
	:twitter:description: Logical Mistakes: Avoid logical mistakes within long expressions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Logical Mistakes
	:og:type: article
	:og:description: Avoid logical mistakes within long expressions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Logical Mistakes.html
	:og:locale: en
Avoid logical mistakes within long expressions. 

Sometimes, the logic is not what it seems. It is important to check the actual impact of every part of the logical expression. Do not hesitate to make a table with all possible cases. If those cases are too numerous, it may be time to rethink the whole expression. 
Inspired by an article from ``Andrey Karpov``.

.. code-block:: php
   
   <?php 
   
   // Always true
   if ($a != 1 || $a != 2) { } 
   
   // $a == 1 is useless
   if ($a == 1 || $a != 2) {}
   
   // Always false
   if ($a == 1 && $a == 2) {}
   
   // $a != 2 is useless
   if ($a == 1 && $a != 2) {}
   
   ?>

See also `Logical Expressions in C/C++. Mistakes Made by Professionals <http://www.viva64.com/en/b/0390/>`_.


Suggestions
___________

* Change the expressions for them to have a real meaning




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/LogicalMistakes                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-logicalmistakes`, :ref:`case-cleverstyle-structures-logicalmistakes`                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


