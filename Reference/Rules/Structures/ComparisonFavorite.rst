.. _structures-comparisonfavorite:


.. _strict-or-relaxed-comparison:

Strict Or Relaxed Comparison
++++++++++++++++++++++++++++

.. meta::
	:description:
		Strict Or Relaxed Comparison: PHP has two comparison styles : strict and relaxed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strict Or Relaxed Comparison
	:twitter:description: Strict Or Relaxed Comparison: PHP has two comparison styles : strict and relaxed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strict Or Relaxed Comparison
	:og:type: article
	:og:description: PHP has two comparison styles : strict and relaxed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strict Or Relaxed Comparison.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ComparisonFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ComparisonFavorite.html","name":"Strict Or Relaxed Comparison","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP has two comparison styles : strict and relaxed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Strict Or Relaxed Comparison.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP has two comparison styles : strict and relaxed. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It is recommended to always use the strict comparison by default, and use the relaxed in case of specific situations.

.. code-block:: php
   
   <?php
   
   // This compares $strict both in terms of value and type
   if ($strict === 3) {
   
   } elseif ($strict == 3) {
       // This compares $strict after an possible type casting. 
       // '3', 3.0 or 3 would all be possible solutions.
   }
   
   ?>

See also `Comparison Operators <https://www.php.net/manual/en/language.operators.comparison.php>`_.

Connex PHP features
-------------------

  + `Comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ComparisonFavorite                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


