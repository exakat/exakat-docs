.. _performances-noconcatinloop:


.. _avoid-concat-in-loop:

Avoid Concat In Loop
++++++++++++++++++++

.. meta::
	:description:
		Avoid Concat In Loop: Concatenations inside a loop generate a lot of temporary variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Concat In Loop
	:twitter:description: Avoid Concat In Loop: Concatenations inside a loop generate a lot of temporary variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Concat In Loop
	:og:type: article
	:og:description: Concatenations inside a loop generate a lot of temporary variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid Concat In Loop.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/NoConcatInLoop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/NoConcatInLoop.html","name":"Avoid Concat In Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Concatenations inside a loop generate a lot of temporary variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid Concat In Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Concatenations inside a loop generate a lot of temporary variables. They are accumulated and tend to raise the memory usage, leading to slower performances.

It is recommended to store the values in an array, and then use `implode() <https://www.php.net/implode>`_ on that array to make the concatenation at once. The effect is positive when the source array has at least 50 elements. 
The same doesn't apply to addition and multiplication, with `array_sum() <https://www.php.net/array_sum>`_ and array_multiply(), as those operations work on the current memory allocation, and don't need to allocate new memory at each step.

.. code-block:: php
   
   <?php
   
   // Concatenation in one operation
   $tmp = array();
   foreach(data_source() as $data) {
       $tmp[] = $data;
   }
   $final = implode('', $tmp);
   
   // Concatenation in many operations
   foreach(data_source() as $data) {
       $final .= $data;
   }
   
   ?>

See also `PHP 7 performance improvements (3/5): Encapsed strings optimization <https://blog.blackfire.io/php-7-performance-improvements-encapsed-strings-optimization.html>`_.

Connex PHP features
-------------------

  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Collect all pieces in an array, then implode() the array in one call.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/NoConcatInLoop                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-performances-noconcatinloop`, :ref:`case-thinkphp-performances-noconcatinloop`                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


