.. _structures-addzero:


.. _adding-zero:

Adding Zero
+++++++++++

.. meta::
	:description:
		Adding Zero: Adding 0 is useless, as 0 is the neutral element for addition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Adding Zero
	:twitter:description: Adding Zero: Adding 0 is useless, as 0 is the neutral element for addition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Adding Zero
	:og:type: article
	:og:description: Adding 0 is useless, as 0 is the neutral element for addition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Adding Zero.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AddZero.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AddZero.html","name":"Adding Zero","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Adding 0 is useless, as 0 is the neutral element for addition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Adding Zero.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Adding 0 is useless, as 0 is the neutral element for addition. Besides, when one of the operands is an integer, PHP silently triggers a cast to integer for the other operand. 

This rule also report using ``+`` with variables, proeprties, etc. which triggers an automated conversion to integer.

It is recommended to make the cast explicit with ``(int)``.

.. code-block:: php
   
   <?php
   
   // Explicit cast
   $a = (int) foo();
   
   // Useless addition
   $a = foo() + 0;
   $a = 0 + foo();
   
   // Also works with minus
   $b = 0 - $c; // drop the 0, but keep the minus
   $b = $c - 0; // drop the 0 and the minus
   
   $a += 0;
   $a -= 0;
   
   $z = '12';
   print +$z + 1;
   
   ?>
Connex PHP features
-------------------

  + `Addition <https://php-dictionary.readthedocs.io/en/latest/dictionary/addition.ini.html>`_
  + `Short Assignations <https://php-dictionary.readthedocs.io/en/latest/dictionary/short-assignation.ini.html>`_


Suggestions
___________

* Remove the +/- 0, may be the whole assignation
* Use an explicit type casting operator (int)




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AddZero                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Rector <ruleset-Rector>`                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-math <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-math.md>`__                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thelia-structures-addzero`, :ref:`case-openemr-structures-addzero`                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


