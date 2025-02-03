.. _classes-differentargumentcounts:

.. _different-argument-counts:

Different Argument Counts
+++++++++++++++++++++++++

.. meta::
	:description:
		Different Argument Counts: Two methods with the same name shall have the same number of compulsory argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Different Argument Counts
	:twitter:description: Different Argument Counts: Two methods with the same name shall have the same number of compulsory argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Different Argument Counts
	:og:type: article
	:og:description: Two methods with the same name shall have the same number of compulsory argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Different Argument Counts.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DifferentArgumentCounts.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DifferentArgumentCounts.html","name":"Different Argument Counts","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Two methods with the same name shall have the same number of compulsory argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Different Argument Counts.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Two methods with the same name shall have the same number of compulsory argument. PHP accepts different number of arguments between two methods, if the extra arguments have default values. Basically, they shall be called interchangeably with the same number of arguments.

The number of compulsory arguments is often mistaken for the same number of arguments. When this is the case, it leads to confusion between the two signatures. It will also create more difficulties when refactoring the signature.

While this code is legit, it is recommended to check if the two signatures could be synchronized, and reduce future surprises.

.. code-block:: php
   
   <?php
   
   class x {
       function foo($a ) {}
   }
   
   class y extends x {
       // This method is compatible with the above, its signature is different
       function foo($a, $b = 1) {}
   }
   
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Extract the extra arguments into other methods
* Remove the extra arguments
* Add the extra arguments to all the signatures




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DifferentArgumentCounts                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


