.. _performances-ellipsismerge:


.. _ellipsis-merge:

Ellipsis Merge
++++++++++++++

.. meta::
	:description:
		Ellipsis Merge: Ellipsis are slower than array_merge().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ellipsis Merge
	:twitter:description: Ellipsis Merge: Ellipsis are slower than array_merge()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ellipsis Merge
	:og:type: article
	:og:description: Ellipsis are slower than array_merge()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Ellipsis Merge.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/EllipsisMerge.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/EllipsisMerge.html","name":"Ellipsis Merge","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Ellipsis are slower than array_merge()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Ellipsis Merge.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Ellipsis are slower than `array_merge() <https://www.php.net/array_merge>`_. 

The speed up is significative when the merge happen inside a loop. There, `array_merge() <https://www.php.net/array_merge>`_ is an order of magnitude faster.

This is a micro optimisation. The larger and numerous the arrays, the better the speed gain. 

.. code-block:: php
   
   <?php
   
   // slow
   $all = array_merge($array1, $array2);
   
   // very slow
   $all = array(...$array1, ...$array2);
   
   ?>
Connex PHP features
-------------------

  + `Merge <https://php-dictionary.readthedocs.io/en/latest/dictionary/merge.ini.html>`_
  + `Ellipsis <https://php-dictionary.readthedocs.io/en/latest/dictionary/ellipsis.ini.html>`_
  + `Micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Suggestions
___________

* Use array_merge()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/EllipsisMerge                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


