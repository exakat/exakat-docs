.. _structures-autounsetforeach:

.. _same-variable-foreach:

Same Variable Foreach
+++++++++++++++++++++

.. meta::
	:description:
		Same Variable Foreach: A foreach which uses its own source as a blind variable is actually broken.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Same Variable Foreach
	:twitter:description: Same Variable Foreach: A foreach which uses its own source as a blind variable is actually broken
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Same Variable Foreach
	:og:type: article
	:og:description: A foreach which uses its own source as a blind variable is actually broken
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Same Variable Foreach.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AutoUnsetForeach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AutoUnsetForeach.html","name":"Same Variable Foreach","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A foreach which uses its own source as a blind variable is actually broken","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Same Variable Foreach.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A foreach which uses its own source as a blind variable is actually broken.

Actually, PHP makes a copy of the source before it starts the loop. As such, the same variable may be used for both source and blind value. 

Of course, this is very confusing, to see the same variables used in very different ways. 

The source will also be destroyed immediately after the blind variable has been turned into a reference.

.. code-block:: php
   
   <?php
   
   $array = range(0, 10);
   foreach($array as $array) {
       print $array.PHP_EOL;
   }
   
   print_r($array); // display number from 0 to 10.
   
   $array = range(0, 10);
   foreach($array as &$array) {
       print $array.PHP_EOL;
   }
   
   print_r($array); // display 10
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Name the source and variable names distinctly




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AutoUnsetForeach                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


