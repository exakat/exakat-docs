.. _structures-mismatchedternary:


.. _mismatched-ternary-alternatives:

Mismatched Ternary Alternatives
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Mismatched Ternary Alternatives: A ternary operator should yield the same type on both branches.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatched Ternary Alternatives
	:twitter:description: Mismatched Ternary Alternatives: A ternary operator should yield the same type on both branches
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatched Ternary Alternatives
	:og:type: article
	:og:description: A ternary operator should yield the same type on both branches
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mismatched Ternary Alternatives.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MismatchedTernary.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MismatchedTernary.html","name":"Mismatched Ternary Alternatives","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"A ternary operator should yield the same type on both branches","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mismatched Ternary Alternatives.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A ternary operator should yield the same type on both branches.

Ternary operator applies a condition, and yield two different results. Those results will then be processed by code that expects the same types. It is recommended to match the types on both branches of the ternary operator.

.. code-block:: php
   
   <?php
   
   // $object may end up in a very unstable state
   $object = ($type == 'Type') ? new $type() : null;
   
   //same result are provided by both alternative, though process is very different
   $result = ($type == 'Addition') ? $a + $b : $a * $b;
   
   //Currently, this is omitted
   $a = 1;
   $result = empty($condition) ? $a : 'default value';
   $result = empty($condition) ? $a : getDefaultValue();
   
   ?>
Connex PHP features
-------------------

  + `Ternary Operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_


Suggestions
___________

* Use compatible data type in both branch of the alternative
* Turn the ternary into a if/then, with different processing




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MismatchedTernary                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.1                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpadsnew-structures-mismatchedternary`, :ref:`case-openemr-structures-mismatchedternary`                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


