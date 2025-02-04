.. _structures-evalusage:


.. _eval()-usage:

Eval() Usage
++++++++++++

.. meta::
	:description:
		Eval() Usage: Using eval() is evil.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Eval() Usage
	:twitter:description: Eval() Usage: Using eval() is evil
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Eval() Usage
	:og:type: article
	:og:description: Using eval() is evil
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Eval() Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EvalUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EvalUsage.html","name":"Eval() Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Using eval() is evil","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Eval() Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Using eval() is evil. 

Using eval() is bad for performances (compilation time), for caches (it won't be compiled), and for security (if it includes external data).
Most of the time, it is possible to replace the code by some standard PHP, like variable variable for accessing a variable for which you have the name.
At worse, including a pregenerated file is faster and cacheable. 

There are several situations where eval() is actually the only solution : 

For PHP 7.0 and later, it is important to put eval() in a try..catch expression.

.. code-block:: php
   
   <?php
       // Avoid using incoming data to build the eval() expression : any filtering error leads to PHP injection
       $mathExpression = $_GET['mathExpression']; 
       $mathExpression = preg_replace('#[^0-9+-*/(/)]#is', '', $mathExpression); // expecting 1+2
       $literalCode = '$a = '.$mathExpression.';';
       eval($literalCode);
       echo $a;
   
       // If the code code given to eval() is known at compile time, it is best to put it inline
       $literalCode = 'phpinfo();';
       eval($literalCode);
   
   ?>

See also `eval <http://www.php.net/eval>`_ and `The Land Where PHP  Uses eval() <https://www.exakat.io/land-where-php-uses-eval/>`_.

Connex PHP features
-------------------

  + `Eval() <https://php-dictionary.readthedocs.io/en/latest/dictionary/eval.ini.html>`_


Suggestions
___________

* Use a dynamic feature of PHP to replace the dynamic code
* Store the code on the disk, and use include
* Replace create_function() with a closure!




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EvalUsage                                                                                                                                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Performances <ruleset-Performances>`, :ref:`Security <ruleset-Security>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-eval <https://github.com/dseguy/clearPHP/tree/master/rules/no-eval.md>`__                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xoops-structures-evalusage`, :ref:`case-mautic-structures-evalusage`                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


