.. _structures-bailoutearly:

.. _bail-out-early:

Bail Out Early
++++++++++++++

.. meta::
	:description:
		Bail Out Early: When using conditions, it is recommended to quit in the current context, and avoid the else clause altogether.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Bail Out Early
	:twitter:description: Bail Out Early: When using conditions, it is recommended to quit in the current context, and avoid the else clause altogether
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Bail Out Early
	:og:type: article
	:og:description: When using conditions, it is recommended to quit in the current context, and avoid the else clause altogether
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Bail Out Early.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/BailOutEarly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/BailOutEarly.html","name":"Bail Out Early","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using conditions, it is recommended to quit in the current context, and avoid the else clause altogether","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Bail Out Early.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When using conditions, it is recommended to quit in the current context, and avoid the else clause altogether. 

The main benefit is to make clear the method applies a condition, and stop immediately when this condition is not satisfied. 
The main sequence is then focused on the important code. 

This analysis works with the ``break``, ``continue``, ``throw`` and ``goto`` keywords too, depending on situations.

.. code-block:: php
   
   <?php
   
   // Bailing out early, low level of indentation
   function foo1($a) {
       if ($a > 0) {
           return false;
       } 
       
       $a++;
       return $a;
   }
   
   // Works with continue too
   foreach($array as $a => $b) {
       if ($a > 0) {
           continue false;
       } 
       
       $a++;
       return $a;
   }
   
   // No need for else
   function foo2($a) {
       if ($a > 0) {
           return false;
       } else {
           $a++;
       }
       
       return $a;
   }
   
   // No need for else : return goes into then. 
   function foo3($a) {
       if ($a < 0) {
           $a++;
       } else {
           return false;
       }
       
       return $a;
   }
   
   // Make a return early, and make the condition visible.
   function foo3($a) {
       if ($a < 0) {
           $a++;
           methodcall();
           functioncall();
       } 
   }
   
   ?>

See also `Avoid nesting too deeply and return early (part 1) <https://github.com/jupeter/clean-code-php#avoid-nesting-too-deeply-and-return-early-part-1>`_ and `Avoid nesting too deeply and return early (part 2) <https://github.com/jupeter/clean-code-php#avoid-nesting-too-deeply-and-return-early-part-2>`_.

Connex PHP features
-------------------

  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Suggestions
___________

* Detect errors, and then, return as soon as possible.
* When a if...then branches are unbalanced, test for the small branch, finish it with return. Then keep the other branch as the main code.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BailOutEarly                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-structures-bailoutearly`, :ref:`case-opencfp-structures-bailoutearly`                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


