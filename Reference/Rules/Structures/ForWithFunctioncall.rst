.. _structures-forwithfunctioncall:


.. _for-using-functioncall:

For Using Functioncall
++++++++++++++++++++++

.. meta::
	:description:
		For Using Functioncall: It is recommended to avoid functioncall in the for() statement.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: For Using Functioncall
	:twitter:description: For Using Functioncall: It is recommended to avoid functioncall in the for() statement
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: For Using Functioncall
	:og:type: article
	:og:description: It is recommended to avoid functioncall in the for() statement
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/For Using Functioncall.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ForWithFunctioncall.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ForWithFunctioncall.html","name":"For Using Functioncall","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is recommended to avoid functioncall in the for() statement","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/For Using Functioncall.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is recommended to avoid functioncall in the `for() <https://www.php.net/manual/en/control-structures.for.php>`_ statement. 

This is `true <https://www.php.net/true>`_ with any kind of functioncall that returns the same value throughout the loop. 

Make sure that the functioncall doesn't change with the loop.

.. code-block:: php
   
   <?php
   
   // Fastest way
   $nb = count($array); 
   for($i = 0; $i < $nb; ++$i) {
       doSomething($i);
   } 
   
   // Same as above, but slow
   for($i = 0; $i < count($array); ++$i) {
       doSomething($i);
   } 
   
   // Same as above, but slow
   foreach($portions as &$portion) {
       // here, array_sum() doesn't depends on the $grade. It should be out of the loop
       $portion = $portion / array_sum($portions);
   } 
   
   $total = array_sum($portion);
   foreach($portion as &$portion) {
       $portion = $portion / $total;
   } 
   
   ?>

See also `PHP for loops and counting arrays <https://electrictoolbox.com/php-for-loop-counting-array/>`_.

Connex PHP features
-------------------

  + `For <https://php-dictionary.readthedocs.io/en/latest/dictionary/for.ini.html>`_


Suggestions
___________

* Call the function once, before the loop
* Replace by a foreach structure




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForWithFunctioncall                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Rector <ruleset-Rector>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-functioncall-in-loop <https://github.com/dseguy/clearPHP/tree/master/rules/no-functioncall-in-loop.md>`__                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


