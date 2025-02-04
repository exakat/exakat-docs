.. _structures-printwithoutparenthesis:


.. _avoid-parenthesis-with-language-construct:

Avoid Parenthesis With Language Construct
+++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Avoid Parenthesis With Language Construct: Avoid Parenthesis for language construct.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Parenthesis With Language Construct
	:twitter:description: Avoid Parenthesis With Language Construct: Avoid Parenthesis for language construct
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Parenthesis With Language Construct
	:og:type: article
	:og:description: Avoid Parenthesis for language construct
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid Parenthesis With Language Construct.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PrintWithoutParenthesis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PrintWithoutParenthesis.html","name":"Avoid Parenthesis With Language Construct","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid Parenthesis for language construct","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid Parenthesis With Language Construct.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid Parenthesis for language construct. Languages constructs are a few PHP native elements, that looks like functions but are not. 

Among other distinction, those elements cannot be directly used as variable function call, and they may be used with or without parenthesis.
The usage of parenthesis actually give some feeling of comfort, it won't prevent PHP from combining those argument with any later operators, leading to unexpected results.

Even if most of the time, usage of parenthesis is legit, it is recommended to avoid them.

.. code-block:: php
   
   <?php
   
   // normal usage of include
   include 'file.php';
   
   // This looks like a function and is not
   include('file2.php');
   
   ?>
Connex PHP features
-------------------

  + `Language Construct <https://php-dictionary.readthedocs.io/en/latest/dictionary/language-construct.ini.html>`_


Suggestions
___________

* Remove the parenthesis




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PrintWithoutParenthesis                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


