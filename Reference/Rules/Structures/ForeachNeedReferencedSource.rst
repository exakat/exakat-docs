.. _structures-foreachneedreferencedsource:


.. _foreach-needs-reference-array:

Foreach Needs Reference Array
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Foreach Needs Reference Array: When using foreach with a reference as value, the source must be a referenced array, which is a variable (or array or property or static property).
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Foreach Needs Reference Array
	:twitter:description: Foreach Needs Reference Array: When using foreach with a reference as value, the source must be a referenced array, which is a variable (or array or property or static property)
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Foreach Needs Reference Array
	:og:type: article
	:og:description: When using foreach with a reference as value, the source must be a referenced array, which is a variable (or array or property or static property)
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Foreach Needs Reference Array.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ForeachNeedReferencedSource.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ForeachNeedReferencedSource.html","name":"Foreach Needs Reference Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using foreach with a reference as value, the source must be a referenced array, which is a variable (or array or property or static property)","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Foreach Needs Reference Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using foreach with a reference as value, the source must be a referenced array, which is a variable (or array or property or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property). 
When the array is the `result <https://www.php.net/result>`_ of an expression, the array is not kept in memory after the foreach loop, and any change made with & are lost.

This will do nothing
This will have an actual effect

.. code-block:: php
   
   <?php
       foreach(array(1,2,3) as &$value) {
           $value *= 2;
       }
   ?>
Connex PHP features
-------------------

  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `References <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Use a referenced array when applying modifications inside a foreach loop




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForeachNeedReferencedSource                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


