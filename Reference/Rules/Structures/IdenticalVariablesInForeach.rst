.. _structures-identicalvariablesinforeach:


.. _identical-variables-in-foreach:

Identical Variables In Foreach
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Identical Variables In Foreach: Do not use the same variable names as a foreach() source and one of its blind variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Identical Variables In Foreach
	:twitter:description: Identical Variables In Foreach: Do not use the same variable names as a foreach() source and one of its blind variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Identical Variables In Foreach
	:og:type: article
	:og:description: Do not use the same variable names as a foreach() source and one of its blind variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Identical Variables In Foreach.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IdenticalVariablesInForeach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IdenticalVariablesInForeach.html","name":"Identical Variables In Foreach","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Do not use the same variable names as a foreach() source and one of its blind variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Identical Variables In Foreach.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Do not use the same variable names as a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ source and one of its blind variables. 

`Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ makes a copy of the original data while working on it : this prevents any interference. Yet, when the source and the blind variable is the same, the source will have changed after the loop.

.. code-block:: php
   
   <?php
   
   // classic way to use a foreach loop
   foreach($array as $key => $value) {
       // doSomething with $key and $value
   }
   
   // unusual way to end up with a name conflict
   foreach($a as $a => [$b, $c, $a]) {
       // doSomething with $a and $a, $b, $c
   }
   
   
   // classic way to use a foreach loop
   foreach($a as $a => $b) {
       // doSomething with $a and $a
   }
   // Now, after the loop, $a is an integer or a string!
   
   ?>
Connex PHP features
-------------------

  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Use a different name for the source of the array and the blind values




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalVariablesInForeach                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
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


