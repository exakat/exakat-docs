.. _structures-nestedloops:

.. _nested-loops:

Nested Loops
++++++++++++

.. meta::
	:description:
		Nested Loops: Nested loops happens when a loop (while, do.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nested Loops
	:twitter:description: Nested Loops: Nested loops happens when a loop (while, do
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nested Loops
	:og:type: article
	:og:description: Nested loops happens when a loop (while, do
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Nested Loops.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NestedLoops.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NestedLoops.html","name":"Nested Loops","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Nested loops happens when a loop (while, do","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Nested Loops.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Nested loops happens when a loop (while, do..while, for, foreach), is used inside another loop. 
Such structure tends to require a lot of processing, as the size of both loops have to be multiplied to estimate the actual payload. They should be avoided as much as possible. This may no be always possible, though.

Nested loops are worth a check for performances reasons, as they will process a lot of times the same instructions.

.. code-block:: php
   
   <?php
   
   // Nested loops
   foreach($array as $a) {
       foreach ($letters as $b) {
           // This is performed count($array) * count($letters) times. 
           doSomething();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `nesting <https://php-dictionary.readthedocs.io/en/latest/dictionary/nesting.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NestedLoops                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


