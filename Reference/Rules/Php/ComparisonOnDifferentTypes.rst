.. _php-comparisonondifferenttypes:


.. _comparison-on-different-types:

Comparison On Different Types
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Comparison On Different Types: This rule reports comparisons and spaceship operator that are used with distinct types.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Comparison On Different Types

	:twitter:description: Comparison On Different Types: This rule reports comparisons and spaceship operator that are used with distinct types

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Comparison On Different Types

	:og:type: article

	:og:description: This rule reports comparisons and spaceship operator that are used with distinct types

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Comparison On Different Types.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ComparisonOnDifferentTypes.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ComparisonOnDifferentTypes.html","name":"Comparison On Different Types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule reports comparisons and spaceship operator that are used with distinct types","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Comparison On Different Types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports comparisons and spaceship operator that are used with distinct types. When the types are distinct, PHP apply silent type juggling, and it may `result <https://www.php.net/result>`_ in unexpected results. 

.. code-block:: php
   
   <?php
   
   1 == 'a';
   
   ?>

Suggestions
___________

* Ensure both operands are using the same type.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ComparisonOnDifferentTypes                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


