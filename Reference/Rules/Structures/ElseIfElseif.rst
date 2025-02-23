.. _structures-elseifelseif:


.. _else-if-versus-elseif:

Else If Versus Elseif
+++++++++++++++++++++

.. meta::
	:description:
		Else If Versus Elseif: Always use elseif instead of else and if.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Else If Versus Elseif
	:twitter:description: Else If Versus Elseif: Always use elseif instead of else and if
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Else If Versus Elseif
	:og:type: article
	:og:description: Always use elseif instead of else and if
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Else If Versus Elseif.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ElseIfElseif.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ElseIfElseif.html","name":"Else If Versus Elseif","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Always use elseif instead of else and if","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Else If Versus Elseif.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Always use elseif instead of else and if. 

The keyword elseif SHOULD be used instead of else if so that all control keywords look like single words". Quoted from the PHP-FIG documentation

.. code-block:: php
   
   <?php
   
   // Using elseif 
   if ($a == 1) { doSomething(); }
   elseif ($a == 2) { doSomethingElseIf(); }
   else { doSomethingElse(); }
   
   // Using else if 
   if ($a == 1) { doSomething(); }
   else if ($a == 2) { doSomethingElseIf(); }
   else { doSomethingElse(); }
   
   // Using else if, no {}
   if ($a == 1)  doSomething(); 
   else if ($a == 2) doSomethingElseIf(); 
   else  doSomethingElse(); 
   
   ?>

See also `elseif/else if <https://www.php.net/manual/en/control-structures.elseif.php>`_.

Connex PHP features
-------------------

  + `If Then Else <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Merge else and if into elseif
* Turn the else expression into a block, and have more than the second if in this block
* Turn the if / else if / else into a switch structure




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ElseIfElseif                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Rector <ruleset-Rector>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-structures-elseifelseif`, :ref:`case-phpdocumentor-structures-elseifelseif`                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


