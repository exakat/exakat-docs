.. _structures-doubleinstruction:


.. _double-instructions:

Double Instructions
+++++++++++++++++++


.. meta::

	:description:

		Double Instructions: Twice the same call in a row.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Double Instructions

	:twitter:description: Double Instructions: Twice the same call in a row

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Double Instructions

	:og:type: article

	:og:description: Twice the same call in a row

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Double Instructions.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DoubleInstruction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DoubleInstruction.html","name":"Double Instructions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Twice the same call in a row","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Double Instructions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Twice the same call in a row. This might be a typo, and the second call is useless. 

It may also be an non-idempotent method: that is, a method which has a different `result <https://www.php.net/result>`_ when called with the same arguments. For example, ``rand()`` or ``fgets()``.

.. code-block:: php
   
   <?php
   
   // repetition of the same command, with the same effect each time. 
   $a = array_merge($b, $c);
   $a = array_merge($b, $c);
   
   // false positive : commands are identical, but the effect is compounded 
   $a = array_merge($a, $c);
   $a = array_merge($a, $c);
   
   ?>
Connex PHP features
-------------------

  + `idempotent <https://php-dictionary.readthedocs.io/en/latest/dictionary/idempotent.ini.html>`_


Suggestions
___________

* Remove double work
* Avoid repetition by using loops, variadic or quantifiers `(dirname($path, 2))`




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DoubleInstruction                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


