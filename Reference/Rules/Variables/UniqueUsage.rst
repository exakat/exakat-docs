.. _variables-uniqueusage:


.. _single-use-variables:

Single Use Variables
++++++++++++++++++++

.. meta::
	:description:
		Single Use Variables: This is the list of variables that are written, then read, and only used once.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Single Use Variables
	:twitter:description: Single Use Variables: This is the list of variables that are written, then read, and only used once
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Single Use Variables
	:og:type: article
	:og:description: This is the list of variables that are written, then read, and only used once
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Single Use Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/UniqueUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/UniqueUsage.html","name":"Single Use Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This is the list of variables that are written, then read, and only used once","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Single Use Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This is the list of variables that are written, then read, and only used once.

Single-use variables may be trimmed down, and the initial expression may be used instead.

Single-use variables may improve readability, when the final expression grows too much with the extra expression. 


.. code-block:: php
   
   <?php
   
   function foo($d) {
       $a = 1;     // $a is used twice
       $b = $a + 2;  // $b is used once
       $c = $a + $b + $d; // $c is also used once
       // $d is an argument, so it's OK.
       
       retrun $c;
   }
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Merge the two expressions into one larger
* Make a second use of the variable
* Inline the code of the expression instead of the variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UniqueUsage                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


