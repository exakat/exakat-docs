.. _complete-solvetraitmethods:


.. _solve-trait-methods:

Solve Trait Methods
+++++++++++++++++++

.. meta::
	:description:
		Solve Trait Methods: This command adds DEFINITION link between trait's method definitions and their usage in classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Solve Trait Methods
	:twitter:description: Solve Trait Methods: This command adds DEFINITION link between trait's method definitions and their usage in classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Solve Trait Methods
	:og:type: article
	:og:description: This command adds DEFINITION link between trait's method definitions and their usage in classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Solve Trait Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SolveTraitMethods.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SolveTraitMethods.html","name":"Solve Trait Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command adds DEFINITION link between trait's method definitions and their usage in classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Solve Trait Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command adds DEFINITION link between trait's method definitions and their usage in classes.

.. code-block:: php
   
   <?php
   
   trait t {
       function foo() {
       
       }
   }
   
   class x {
       use t { t::foo as foo2; };
       
       function bar() {
           // Link to foo() in trait t
           $this->foo();
           // Link to foo() in trait t, thanks to 'as'
           $this->foo2();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SolveTraitMethods                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


