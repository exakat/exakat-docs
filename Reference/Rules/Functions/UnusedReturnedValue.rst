.. _functions-unusedreturnedvalue:


.. _unused-returned-value:

Unused Returned Value
+++++++++++++++++++++

.. meta::
	:description:
		Unused Returned Value: The function called returns a value, which is ignored.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Returned Value
	:twitter:description: Unused Returned Value: The function called returns a value, which is ignored
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Returned Value
	:og:type: article
	:og:description: The function called returns a value, which is ignored
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Returned Value.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedReturnedValue.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedReturnedValue.html","name":"Unused Returned Value","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The function called returns a value, which is ignored","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Returned Value.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The function called returns a value, which is ignored. 

Usually, this is a sign of dead code, or a missed check on the results of the functioncall. At times, it may be a valid call if the function has voluntarily no return value. 

It is recommended to add a check on the return value, or remove the call. 



Note that this analysis ignores functions that return void (same meaning that PHP 7.1 : return ; or no return in the function body).

.. code-block:: php
   
   <?php
   
   // simplest form
   function foo() {
       return 1;
   }
   
   foo();
   
   // In case of multiple return, any one that returns something means that return value is meaningful
   function bar() {
       if (rand(0, 1)) {
           return 1;
       } else {
           return ;
       }
   }
   
   bar();
   
   ?>
Connex PHP features
-------------------

  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnusedReturnedValue                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Dead code <ruleset-Dead-code>`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.5                                                                                                                   |
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


