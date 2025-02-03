.. _structures-onelinetwoinstructions:


.. _several-instructions-on-the-same-line:

Several Instructions On The Same Line
+++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Several Instructions On The Same Line: Usually, instructions do not share their line : one instruction, one line.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Several Instructions On The Same Line

	:twitter:description: Several Instructions On The Same Line: Usually, instructions do not share their line : one instruction, one line

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Several Instructions On The Same Line

	:og:type: article

	:og:description: Usually, instructions do not share their line : one instruction, one line

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Several Instructions On The Same Line.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OneLineTwoInstructions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OneLineTwoInstructions.html","name":"Several Instructions On The Same Line","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usually, instructions do not share their line : one instruction, one line","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Several Instructions On The Same Line.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Usually, instructions do not share their line : one instruction, one line. 

This is good for readability, and help at understanding the code. This is especially important when fast-reading the code to find some special situation, where such double-meaning line way have an impact.

.. code-block:: php
   
   <?php
   
   switch ($x) {
       // Is it a fallthrough or not ? 
       case 1:
           doSomething(); break;
   
       // Easily spotted break.
       case 1:
           doSomethingElse(); 
           break;
   
       default : 
           doDefault(); 
           break;
   }
   
   ?>

See also `Object Calisthenics, rule # 5 <http://williamdurand.fr/2013/06/03/object-calisthenics/#one-dot-per-line>`_.


Suggestions
___________

* Add new lines, so that one expression is on one line




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneLineTwoInstructions                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-structures-onelinetwoinstructions`, :ref:`case-tine20-structures-onelinetwoinstructions`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


