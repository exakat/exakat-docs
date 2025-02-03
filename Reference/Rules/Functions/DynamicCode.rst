.. _functions-dynamiccode:


.. _function-with-dynamic-code:

Function With Dynamic Code
++++++++++++++++++++++++++

.. meta::
	:description:
		Function With Dynamic Code: Mark a method, function, closure, arrow function that includes dynamic code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Function With Dynamic Code
	:twitter:description: Function With Dynamic Code: Mark a method, function, closure, arrow function that includes dynamic code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Function With Dynamic Code
	:og:type: article
	:og:description: Mark a method, function, closure, arrow function that includes dynamic code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Function With Dynamic Code.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/DynamicCode.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/DynamicCode.html","name":"Function With Dynamic Code","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark a method, function, closure, arrow function that includes dynamic code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Function With Dynamic Code.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mark a method, function, `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, arrow function that includes dynamic code. 

Dynamic code is based on usage of include(), require(), require_once() and include(), `extract() <https://www.php.net/extract>`_ and eval(). 

This is a support rule, to help omits some special cases in other rules.

.. code-block:: php
   
   <?php
   
   // Function with dynamic code
   function foo($x) {
       include $x;
       return $y;
   }
   
   // Static coe Function
   function foo($x) {
       return $y + $x;
   }
   
   ?>
Connex PHP features
-------------------

  + `dynamic-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DynamicCode                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


