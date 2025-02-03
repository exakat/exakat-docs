.. _performances-skipemptyarray:

.. _skip-empty-array-when-merging:

Skip Empty Array When Merging
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Skip Empty Array When Merging: When merging arrays that were collected, it is faster to skip the empty arrays, rather than let ``array_merge()`` process them.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Skip Empty Array When Merging
	:twitter:description: Skip Empty Array When Merging: When merging arrays that were collected, it is faster to skip the empty arrays, rather than let ``array_merge()`` process them
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Skip Empty Array When Merging
	:og:type: article
	:og:description: When merging arrays that were collected, it is faster to skip the empty arrays, rather than let ``array_merge()`` process them
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Skip Empty Array When Merging.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SkipEmptyArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SkipEmptyArray.html","name":"Skip Empty Array When Merging","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"When merging arrays that were collected, it is faster to skip the empty arrays, rather than let ``array_merge()`` process them","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Skip Empty Array When Merging.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When merging arrays that were collected, it is faster to skip the empty arrays, rather than let ``array_merge()`` process them. This also works with `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_.

This is a micro-optimisation. It is more efficient with larger arrays.

.. code-block:: php
   
   <?php
   
   $all = [];
   foreach($source as $array) {
   	// $array is an array in this example
   	if (empty($array)) {
   		continue;
   	}
   	
   	$all[] = $array;
   }
   
   $all = array_merge(...$all);
   
   ?>
Connex PHP features
-------------------

  + `merge <https://php-dictionary.readthedocs.io/en/latest/dictionary/merge.ini.html>`_
  + `performance <https://php-dictionary.readthedocs.io/en/latest/dictionary/performance.ini.html>`_
  + `micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SkipEmptyArray                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


