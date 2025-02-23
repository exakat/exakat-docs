.. _arrays-negativestart:


.. _negative-start-index-in-array:

Negative Start Index In Array
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Negative Start Index In Array: Negative starting index in arrays changed in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Negative Start Index In Array
	:twitter:description: Negative Start Index In Array: Negative starting index in arrays changed in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Negative Start Index In Array
	:og:type: article
	:og:description: Negative starting index in arrays changed in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Negative Start Index In Array.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/NegativeStart.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/NegativeStart.html","name":"Negative Start Index In Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Negative starting index in arrays changed in PHP 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Negative Start Index In Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Negative starting index in arrays changed in PHP 8.0. Until then, they were ignored, and automatic index started always at 0. Since PHP 8.0, the next index is calculated.

The behavior will `break <https://www.php.net/manual/en/control-structures.break.php>`_ code that relies on automatic index in arrays, when a negative index is used for a starter.

.. code-block:: php
   
   <?php
   
   $x = [-5 => 2];
   $x[] = 3;
   
   print_r($x);
   
   /*
   PHP 7.4 and older 
   Array
   (
       [-5] => 2
       [0] => 3
   )
   */
   
   /*
   PHP 8.0 and more recent
   Array
   (
       [-5] => 2
       [-4] => 3
   )
   */
   
   ?>

See also `PHP RFC: Arrays starting with a negative index <https://wiki.php.net/rfc/negative_array_index>`_.

Connex PHP features
-------------------

  + `Index <https://php-dictionary.readthedocs.io/en/latest/dictionary/index.ini.html>`_


Suggestions
___________

* Explicitly create the index, instead of using the automatic indexing
* Add an explicit index of 0 in the initial array, to set the automatic process in the right track
* Avoid using specified index in array, conjointly with automatic indexing.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Arrays/NegativeStart                                                                                                                                                                    |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.1.9                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and older                                                                                                                                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0                                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


