.. _structures-uselessnullcoalesce:

.. _useless-null-coalesce:

Useless Null Coalesce
+++++++++++++++++++++

.. meta::
	:description:
		Useless Null Coalesce: When the type system ensure the condition is never null, the operator becomes useless.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Null Coalesce
	:twitter:description: Useless Null Coalesce: When the type system ensure the condition is never null, the operator becomes useless
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Null Coalesce
	:og:type: article
	:og:description: When the type system ensure the condition is never null, the operator becomes useless
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Null Coalesce.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessNullCoalesce.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessNullCoalesce.html","name":"Useless Null Coalesce","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When the type system ensure the condition is never null, the operator becomes useless","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Null Coalesce.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When the type system ensure the condition is never null, the operator becomes useless. 

This is particularly true for properties (`static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not) and returntype of methods and functions. And, to a lesser extend, to variables and parameters.

.. code-block:: php
   
   <?php
   
   function foo(A $a, ?B $b) {
       // $a is never null, so this is OK
       $a ?? 'a';
       
       // $b might be null, so this is OK
       $b ?? 'b';
   }
   
   ?>

See also `Null coalescing operator <https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.null-coalesce-op>`_.

Connex PHP features
-------------------

  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_


Suggestions
___________

* Remove the ?? operator
* Switch to a ?: operator
* Updated the properties to accept NULL as a possible type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessNullCoalesce                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


