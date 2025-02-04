.. _classes-swappedarguments:


.. _swapped-arguments:

Swapped Arguments
+++++++++++++++++

.. meta::
	:description:
		Swapped Arguments: Overwritten methods must be compatible, but argument names is not part of that compatibility.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Swapped Arguments
	:twitter:description: Swapped Arguments: Overwritten methods must be compatible, but argument names is not part of that compatibility
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Swapped Arguments
	:og:type: article
	:og:description: Overwritten methods must be compatible, but argument names is not part of that compatibility
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Swapped Arguments.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/SwappedArguments.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/SwappedArguments.html","name":"Swapped Arguments","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Overwritten methods must be compatible, but argument names is not part of that compatibility","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Swapped Arguments.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Overwritten methods must be compatible, but argument names is not part of that compatibility.

Methods with the same name, in two classes of the same hierarchy, must be compatible for typehint, default value, reference. The name of the argument is not taken into account when checking such compatibility, at least until PHP 7.4.
This analysis reports argument lists that differs in ordering. This analysis doesn't report argument lists that also differs in argument names.

.. code-block:: php
   
   <?php
   
   class x {
       function foo($a, $b) {}
       
       function bar($a, $b) {}
   }
   
   class y extends x {
       // foo is compatible (identical) with the above class
       function foo($a, $b) {}
       
       // bar is compatible with the above class, yet, the argument might not receive what they expect.
       function bar($b, $a) {}
   }
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Make sure the names of the argument are in the same order in all classes and interfaces




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/SwappedArguments                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


