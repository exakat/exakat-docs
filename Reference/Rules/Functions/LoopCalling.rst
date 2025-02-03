.. _functions-loopcalling:

.. _functions-in-loop-calls:

Functions In Loop Calls
+++++++++++++++++++++++

.. meta::
	:description:
		Functions In Loop Calls: The following functions call each-other in a loop fashion : A -> B -> A.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Functions In Loop Calls
	:twitter:description: Functions In Loop Calls: The following functions call each-other in a loop fashion : A -> B -> A
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Functions In Loop Calls
	:og:type: article
	:og:description: The following functions call each-other in a loop fashion : A -> B -> A
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Functions In Loop Calls.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/LoopCalling.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/LoopCalling.html","name":"Functions In Loop Calls","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following functions call each-other in a loop fashion : A -> B -> A","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Functions In Loop Calls.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The following functions call each-other in a loop fashion : A -> B -> A.

When those functions have no other interaction, the code is useless and should be dropped.



Loops of size 2, 3 and 4 function are supported by this analyzer.

.. code-block:: php
   
   <?php
   
   function foo1($a) {
       if ($a < 1000) {
           return foo2($a + 1);
       }
       return $a;
   }
   
   function foo2($a) {
       if ($a < 1000) {
           return foo1($a + 1);
       }
       return $a;
   }
   
   // if foo1 nor foo2 are called, then this is dead code. 
   // if foo1 or foo2 are called, this recursive call should be investigated.
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `recursion <https://php-dictionary.readthedocs.io/en/latest/dictionary/recursion.ini.html>`_


Suggestions
___________

* Drop all the functions in the loop, as they are dead code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/LoopCalling                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


