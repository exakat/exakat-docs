.. _structures-inconsistentelseif:

.. _inconsistent-elseif:

Inconsistent Elseif
+++++++++++++++++++

.. meta::
	:description:
		Inconsistent Elseif: Chaining if/elseif requires a consistent string of conditions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inconsistent Elseif
	:twitter:description: Inconsistent Elseif: Chaining if/elseif requires a consistent string of conditions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inconsistent Elseif
	:og:type: article
	:og:description: Chaining if/elseif requires a consistent string of conditions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Inconsistent Elseif.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InconsistentElseif.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InconsistentElseif.html","name":"Inconsistent Elseif","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Chaining if\/elseif requires a consistent string of conditions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Inconsistent Elseif.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Chaining if/elseif requires a consistent string of conditions. The conditions are executed one after the other, and the conditions shouldn't overlap.

This analysis reports chains of elseif that don't share a common variable (or array, or property, etc.. ). As such, testing different conditions are consistent.

.. code-block:: php
   
   <?php
   
   // $a is always common, so situations are mutually exclusive
   if ($a === 1) {
       doSomething();
   } else if ($a > 1) {
       doSomethingElse();
   } else {
       doSomethingDefault();
   }
   
   // $a is always common, so situations are mutually exclusive
   // although, it may be worth checking the consistency here
   if ($a->b === 1) {
       doSomething();
   } else if ($a->c > 1) {
       doSomethingElse();
   } else {
       doSomethingDefault();
   }
   
   // if $a === 1, then $c doesn't matter? 
   // This happens, but then logic doesn't appear in the code.
   if ($a === 1) {
       doSomething();
   } else if ($c > 1) {
       doSomethingElse();
   } else {
       doSomethingDefault();
   }
   
   ?>
Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InconsistentElseif                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


