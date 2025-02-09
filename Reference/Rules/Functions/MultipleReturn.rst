.. _functions-multiplereturn:


.. _multiple-returns:

Multiple Returns
++++++++++++++++

.. meta::
	:description:
		Multiple Returns: Functions and methods that have multiple return statement.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Returns
	:twitter:description: Multiple Returns: Functions and methods that have multiple return statement
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Returns
	:og:type: article
	:og:description: Functions and methods that have multiple return statement
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Returns.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MultipleReturn.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MultipleReturn.html","name":"Multiple Returns","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Functions and methods that have multiple return statement","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Returns.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Functions and methods that have multiple return statement. 

This makes it difficult to maintain : since the function may be short-circuited early, some later instruction may be omitted.

Ideally, guard clauses, which check if arguments are valid or not at the beginning of the method are the only `exception <https://www.php.net/exception>`_ to this rule.
Currently, the `engine <https://www.php.net/engine>`_ doesn't spot guard clauses.

.. code-block:: php
   
   <?php
   
   function foo() {
       // This is a guard clause, that checks arguments. 
       if ($a < 0) {
           return false;
       }
       
       $b = 0;
       for($i = 0; $i < $a; $i++) {
           $b += bar($i);
       }
       
       return $b;
   }
   ?>

See also `Single Function Exit Point <http://wiki.c2.com/?SingleFunctionExitPoint>`_.

Connex PHP features
-------------------

  + `Return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MultipleReturn                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


