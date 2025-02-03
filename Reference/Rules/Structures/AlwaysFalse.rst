.. _structures-alwaysfalse:

.. _comparison-is-always-the-same:

Comparison Is Always The Same
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Comparison Is Always The Same: Based on the incoming type of arguments, the comparison always yields the same value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Comparison Is Always The Same
	:twitter:description: Comparison Is Always The Same: Based on the incoming type of arguments, the comparison always yields the same value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Comparison Is Always The Same
	:og:type: article
	:og:description: Based on the incoming type of arguments, the comparison always yields the same value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Comparison Is Always The Same.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AlwaysFalse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AlwaysFalse.html","name":"Comparison Is Always The Same","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Based on the incoming type of arguments, the comparison always yields the same value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Comparison Is Always The Same.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Based on the incoming type of arguments, the comparison always yields the same value. The whole condition might be useless.

.. code-block:: php
   
   <?php
   
   function foo(array $a) {
       // This will always fail
       if ($a === 1) {
           
       } elseif (is_int($a)) {
       
       }
   
       // This will always succeed
       if ($a !== null) {
           
       } elseif (is_null($a)) {
           
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Remove the constant condition and its corresponding blocks
* Make the constant condition variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AlwaysFalse                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


