.. _structures-mixedconcatinterpolation:


.. _mixed-concat-and-interpolation:

Mixed Concat And Interpolation
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Mixed Concat And Interpolation: Mixed usage of concatenation and string interpolation is error prone.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mixed Concat And Interpolation
	:twitter:description: Mixed Concat And Interpolation: Mixed usage of concatenation and string interpolation is error prone
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mixed Concat And Interpolation
	:og:type: article
	:og:description: Mixed usage of concatenation and string interpolation is error prone
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mixed Concat And Interpolation.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MixedConcatInterpolation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MixedConcatInterpolation.html","name":"Mixed Concat And Interpolation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mixed usage of concatenation and string interpolation is error prone","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mixed Concat And Interpolation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mixed usage of concatenation and string interpolation is `error <https://www.php.net/error>`_ prone. It is harder to read, and leads to overlooking the concatenation or the interpolation.

Fixing this issue has no impact on the output. It makes code less `error <https://www.php.net/error>`_ prone.

There are some situations where using concatenation are compulsory : when using a constant, calling a function, running a complex expression or make use of the escape sequence. You may also consider pushing the storing of such expression in a local variable.



.. code-block:: php
   
   <?php
   
   // Concatenation string
   $a = $b . 'c' . $d;
   
   // Interpolation strings
   $a = "{$b}c{$d}";   // regular form
   $a = "{$b}c$d";     // irregular form
   
   // Mixed Concatenation and Interpolation string
   $a = "{$b}c" . $d;
   $a = $b . "c$d";
   $a = $b . "c{$d}";
   
   // Mixed Concatenation and Interpolation string with constant
   $a = "{$b}c" . CONSTANT;
   
   ?>
Connex PHP features
-------------------

  + `Interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/interpolation.ini.html>`_
  + `Concatenation <https://php-dictionary.readthedocs.io/en/latest/dictionary/concat.ini.html>`_


Suggestions
___________

* Only use one type of variable usage : either interpolation, or concatenation




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MixedConcatInterpolation                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Coding conventions <ruleset-Coding-conventions>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-structures-mixedconcatinterpolation`, :ref:`case-edusoho-structures-mixedconcatinterpolation`       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


