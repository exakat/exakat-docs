.. _structures-unconditionloopbreak:


.. _unconditional-break-in-loop:

Unconditional Break In Loop
+++++++++++++++++++++++++++

.. meta::
	:description:
		Unconditional Break In Loop: An unconditional break in a loop creates dead code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unconditional Break In Loop
	:twitter:description: Unconditional Break In Loop: An unconditional break in a loop creates dead code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unconditional Break In Loop
	:og:type: article
	:og:description: An unconditional break in a loop creates dead code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unconditional Break In Loop.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnconditionLoopBreak.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnconditionLoopBreak.html","name":"Unconditional Break In Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"An unconditional break in a loop creates dead code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unconditional Break In Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

An unconditional `break <https://www.php.net/manual/en/control-structures.break.php>`_ in a loop creates dead code. Since the `break <https://www.php.net/manual/en/control-structures.break.php>`_ is directly in the body of the loop, it is always executed, creating a strange loop that can only run once. 

Here, `break <https://www.php.net/manual/en/control-structures.break.php>`_ may also be a return, a goto or a `continue <https://www.php.net/manual/en/control-structures.continue.php>`_. They all branch out of the loop. Such statement are valid, but should be moderated with a condition.

.. code-block:: php
   
   <?php
   
   // return in loop should be in 
   function summAll($array) {
       $sum = 0;
       
       foreach($array as $a) {
           // Stop at the first error
           if (is_string($a)) {
               return $sum;
           }
           $sum += $a;
       }
       
       return $sum;
   }
   
   // foreach loop used to collect first element in array
   function getFirst($array) {
       foreach($array as $a) {
           return $a;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_
  + `Break <https://php-dictionary.readthedocs.io/en/latest/dictionary/break.ini.html>`_


Suggestions
___________

* Remove the loop and call the content of the loop once.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnconditionLoopBreak                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.16                                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-livezilla-structures-unconditionloopbreak`, :ref:`case-mediawiki-structures-unconditionloopbreak`                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


