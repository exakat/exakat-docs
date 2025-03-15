.. _functions-methodisnotanif:


.. _method-is-not-an-if:

Method Is Not An If
+++++++++++++++++++

.. meta::
	:description:
		Method Is Not An If: When a method consists only in one if statement, it might be worth refactoring.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Is Not An If
	:twitter:description: Method Is Not An If: When a method consists only in one if statement, it might be worth refactoring
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Is Not An If
	:og:type: article
	:og:description: When a method consists only in one if statement, it might be worth refactoring
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Is Not An If.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MethodIsNotAnIf.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MethodIsNotAnIf.html","name":"Method Is Not An If","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"When a method consists only in one if statement, it might be worth refactoring","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Is Not An If.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When a method consists only in one if statement, it might be worth refactoring. 

Each of the blocks of the if/then structure may be turned into their own method, so has to keep operations distinct. 

Then, the condition can be used as part of a larger method.

.. code-block:: php
   
   <?php
   
   function foo($a) {
   	if ($a === 1) {
   		return 1;
   	} else {
   		return 2;
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_
  + `If Then Else <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Export the blocks to distinct functions
* Bail out early




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MethodIsNotAnIf                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


