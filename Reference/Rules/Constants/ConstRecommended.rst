.. _constants-constrecommended:


.. _use-const:

Use const
+++++++++

.. meta::
	:description:
		Use const: The const keyword may be used to define constant, just like the define() function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use const
	:twitter:description: Use const: The const keyword may be used to define constant, just like the define() function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use const
	:og:type: article
	:og:description: The const keyword may be used to define constant, just like the define() function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use const.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConstRecommended.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConstRecommended.html","name":"Use const","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The const keyword may be used to define constant, just like the define() function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use const.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The const keyword may be used to define constant, just like the `define() <https://www.php.net/define>`_ function. 

When defining a constant, it is recommended to use 'const' when the features of the constant are not dynamical (name or value are known at compile time). 

This way, constant will be defined at compile time, and not at execution time. 

`define() <https://www.php.net/define>`_ function is useful when the constant is not known at compile time, or when case sensitivity is necessary.

.. code-block:: php
   
   <?php
     //Do
     const A = 1;
     // Don't 
     define('A', 1);
     
   ?>

See also `Syntax <https://www.php.net/manual/en/language.constants.syntax.php>`_.

Connex PHP features
-------------------

  + `const <https://php-dictionary.readthedocs.io/en/latest/dictionary/const.ini.html>`_
  + `define <https://php-dictionary.readthedocs.io/en/latest/dictionary/define.ini.html>`_


Suggestions
___________

* Use const instead of define()




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConstRecommended                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpmyadmin-constants-constrecommended`, :ref:`case-piwigo-constants-constrecommended`                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


