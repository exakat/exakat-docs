.. _variables-inconsistentusage:


.. _inconsistent-variable-usage:

Inconsistent Variable Usage
+++++++++++++++++++++++++++


.. meta::

	:description:

		Inconsistent Variable Usage: Those variables are used in various and inconsistent ways.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Inconsistent Variable Usage

	:twitter:description: Inconsistent Variable Usage: Those variables are used in various and inconsistent ways

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Inconsistent Variable Usage

	:og:type: article

	:og:description: Those variables are used in various and inconsistent ways

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Inconsistent Variable Usage.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/InconsistentUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/InconsistentUsage.html","name":"Inconsistent Variable Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those variables are used in various and inconsistent ways","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Inconsistent Variable Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those variables are used in various and inconsistent ways. It is difficult to understand if they are an array, an object or a scalar variable.

.. code-block:: php
   
   <?php
   
   // $a is an array, then $b is a string.
   $a = ['a', 'b', 'c'];
   $b = implode('-', $a);
   
   // $a is an array, then it is a string.
   $a = ['a', 'b', 'c'];
   $a = implode('-', $a);
   
   ?>

Suggestions
___________

* Keep one type for each variable. This keeps the code readable. 
* Give different names to variables with different types.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/InconsistentUsage                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-variables-inconsistentusage`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


