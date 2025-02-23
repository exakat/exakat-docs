.. _structures-sameconditions:


.. _same-conditions-in-condition:

Same Conditions In Condition
++++++++++++++++++++++++++++

.. meta::
	:description:
		Same Conditions In Condition: At least two consecutive if/then structures use identical conditions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Same Conditions In Condition
	:twitter:description: Same Conditions In Condition: At least two consecutive if/then structures use identical conditions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Same Conditions In Condition
	:og:type: article
	:og:description: At least two consecutive if/then structures use identical conditions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Same Conditions In Condition.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SameConditions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SameConditions.html","name":"Same Conditions In Condition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"At least two consecutive if\/then structures use identical conditions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Same Conditions In Condition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

At least two consecutive if/then structures use identical conditions. The latter will probably be ignored.

This analysis returns `false <https://www.php.net/false>`_ positive when there are attempt to fix a situation, or to call an alternative solution. 

Conditions that are shared between if structures, but inside a logical OR expression are also detected.

.. code-block:: php
   
   <?php
   
   if ($a == 1) { doSomething(); }
   elseif ($b == 1) { doSomething(); }
   elseif ($c == 1) { doSomething(); }
   elseif ($a == 1) { doSomething(); }
   else {}
   
   // Also works on if then else if chains
   if ($a == 1) { doSomething(); }
   else if ($b == 1) { doSomething(); }
   else if ($c == 1) { doSomething(); }
   else if ($a == 1) { doSomething(); }
   else {}
   
   // Also works on if then else if chains
   // Here, $a is common and sufficient in both conditions
   if ($a || $b) { doSomething(); } 
   elseif ($a || $c) { doSomethingElse(); } 
   
   // This sort of situation generate false postive. 
   $config = load_config_from_commandline();
   if (empty($config)) {
       $config = load_config_from_file();
       if (empty($config)) {
           $config = load_default_config();
       }
   }
   
   ?>

Suggestions
___________

* Merge the two conditions into one
* Make the two conditions different




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SameConditions                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-structures-sameconditions`, :ref:`case-typo3-structures-sameconditions`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


