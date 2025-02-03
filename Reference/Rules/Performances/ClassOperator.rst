.. _performances-classoperator:

.. _scope-resolution-operator:

Scope Resolution Operator
+++++++++++++++++++++++++

.. meta::
	:description:
		Scope Resolution Operator: The scope resolution operator `::class` is faster than a call to get_class() function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Scope Resolution Operator
	:twitter:description: Scope Resolution Operator: The scope resolution operator `::class` is faster than a call to get_class() function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Scope Resolution Operator
	:og:type: article
	:og:description: The scope resolution operator `::class` is faster than a call to get_class() function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Scope Resolution Operator.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ClassOperator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ClassOperator.html","name":"Scope Resolution Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The scope resolution operator `::class` is faster than a call to get_class() function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Scope Resolution Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The scope resolution operator `\:\:class` is faster than a call to `get_class() <https://www.php.net/get_class>`_ function.

It is also possible to replace `get_class()` by `static\:\:class` to get the name of the calling class.

.. code-block:: php
   
   <?php
   
   $a = new stdClass();
   
   echo $a::class;
   
   // identical to 
   echo get_class($a);
   
   class x {
       function foo() { echo static::class; }
   }
   
   class y extends x {}
   
   // static will resolve to y here
   (new y)->foo();
   
   ?>

See also `get_class <https://www.php.net/manual/fr/function.get-class.php>`_..

Connex PHP features
-------------------

  + `scope-resolution-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/scope-resolution-operator.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Use the `::class` operator instead of the call to get_class()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/ClassOperator                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


