.. _structures-arraymergeandvariadic:


.. _array\_merge()-and-variadic:

array_merge() And Variadic
++++++++++++++++++++++++++

.. meta::
	:description:
		array_merge() And Variadic: Always check the presence of values in a variadic variable, before using it with array_merge() and array_merge_recursive().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: array_merge() And Variadic
	:twitter:description: array_merge() And Variadic: Always check the presence of values in a variadic variable, before using it with array_merge() and array_merge_recursive()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: array_merge() And Variadic
	:og:type: article
	:og:description: Always check the presence of values in a variadic variable, before using it with array_merge() and array_merge_recursive()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/array_merge() And Variadic.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeAndVariadic.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeAndVariadic.html","name":"array_merge() And Variadic","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"Always check the presence of values in a variadic variable, before using it with array_merge() and array_merge_recursive()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/array_merge() And Variadic.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Always check the presence of values in a variadic variable, before using it with `array_merge() <https://www.php.net/array_merge>`_ and `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_.

Before PHP 7.4, `array_merge() <https://www.php.net/array_merge>`_ and `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_ complained when no argument was provided. As such, using the spread operator `...` on an empty `array() <https://www.php.net/array>`_ would yield no argument, and an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   $b = array_merge(...$x);
   
   ?>
Related PHP errors 
-------------------

  + `array_merge() expects at least 1 parameter, 0 given <https://php-errors.readthedocs.io/en/latest/messages/array_merge%28%29-expects-at-least-1-parameter%2C-0-given.html>`_



Connex PHP features
-------------------

  + `variadic <https://php-dictionary.readthedocs.io/en/latest/dictionary/variadic.ini.html>`_


Suggestions
___________

* Add a check to the spread variable to ensure it is not empty
* Append an empty array to to the spread variable to ensure it is not empty




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/ArrayMergeAndVariadic                                                                                        |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.9.2                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.4 and older                                                                                                  |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/array_merge_and_variadic.html>`__      |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                               |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


