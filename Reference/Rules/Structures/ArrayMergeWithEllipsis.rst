.. _structures-arraymergewithellipsis:


.. _array\_merge-with-ellipsis:

array_merge With Ellipsis
+++++++++++++++++++++++++

.. meta::
	:description:
		array_merge With Ellipsis: Ellipsis, or .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: array_merge With Ellipsis
	:twitter:description: array_merge With Ellipsis: Ellipsis, or 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: array_merge With Ellipsis
	:og:type: article
	:og:description: Ellipsis, or 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/array_merge With Ellipsis.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeWithEllipsis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeWithEllipsis.html","name":"array_merge With Ellipsis","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Ellipsis, or ","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/array_merge With Ellipsis.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Ellipsis, or `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_, returns a `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ when the operand array is empty. This doesn't suit `array_merge() <https://www.php.net/array_merge>`_. 

It is recommended to use a coalesce operator, to handle graciously an empty array : use an empty array as default value.

This applies to the following PHP functions : 

* `array_merge() <https://www.php.net/array_merge>`_
* `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_
* `array_diff() <https://www.php.net/array_diff>`_
* `array_diff_assoc() <https://www.php.net/array_diff_assoc>`_
* `array_diff_key() <https://www.php.net/array_diff_key>`_
* `array_diff_uassoc() <https://www.php.net/array_diff_uassoc>`_

.. code-block:: php
   
   <?php
   
   // Correct usage of array_merge and ellipsis
   $a = [ [1,2], [3,4]];
   $b = array_merge(...$a);
   
   // Notee the nested array
   $a = [ ];
   $b = array_merge(...$a ?: [[]] );
   
   // Yield an error because $a is empty
   $a = [ ];
   $b = array_merge(...$a);
   
   ?>

Suggestions
___________

* Use one of the coalesce operator to default to an empty array, avoiding a runtime warning.
* Check the content of the expanded array before using it




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeWithEllipsis                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.6                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


