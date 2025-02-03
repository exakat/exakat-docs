.. _performances-cachevariableoutsideloop:


.. _cache-variable-outside-loop:

Cache Variable Outside Loop
+++++++++++++++++++++++++++


.. meta::

	:description:

		Cache Variable Outside Loop: Avoid recalculating constant values inside the loop.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Cache Variable Outside Loop

	:twitter:description: Cache Variable Outside Loop: Avoid recalculating constant values inside the loop

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Cache Variable Outside Loop

	:og:type: article

	:og:description: Avoid recalculating constant values inside the loop

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cache Variable Outside Loop.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/CacheVariableOutsideLoop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/CacheVariableOutsideLoop.html","name":"Cache Variable Outside Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid recalculating constant values inside the loop","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cache Variable Outside Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid recalculating constant values inside the loop.

Do the calculation once, outside the loop, and then reuse the value in the body of the loop. 

One of the classic example if doing ``count($array)`` in a ``for`` loop : since the source is constant during the loop, the `result <https://www.php.net/result>`_ of `count() <https://www.php.net/count>`_ is always the same. 

Depending on the load of the called method, this may increase the speed of the loop from little to enormously.

This analysis works on all the loops: while, do...while, foreach and for.


.. code-block:: php
   
   <?php
   
   $path = '/some/path';
   $fullpath = realpath("$path/more/dirs/");
   foreach($files as $file) {
       // Only moving parts are used in the loop
       copy($file, $fullpath.$file);
   }
   
   $path = '/some/path';
   foreach($files as $file) {
       // $fullpath is calculated each loop
       $fullpath = realpath("$path/more/dirs/");
       copy($file, $fullpath.$file);
   }
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `for <https://php-dictionary.readthedocs.io/en/latest/dictionary/for.ini.html>`_
  + `while <https://php-dictionary.readthedocs.io/en/latest/dictionary/while.ini.html>`_
  + `do-while <https://php-dictionary.readthedocs.io/en/latest/dictionary/do-while.ini.html>`_


Suggestions
___________

* Store non-blind variables in local variables or properties before the loop.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/CacheVariableOutsideLoop                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.8                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


