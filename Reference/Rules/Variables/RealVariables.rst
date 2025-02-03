.. _variables-realvariables:

.. _real-variables:

Real Variables
++++++++++++++

.. meta::
	:description:
		Real Variables: Inventory of real variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Real Variables
	:twitter:description: Real Variables: Inventory of real variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Real Variables
	:og:type: article
	:og:description: Inventory of real variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Real Variables.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/RealVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/RealVariables.html","name":"Real Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Inventory of real variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Real Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Inventory of real variables. Global, `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ and property declarations are skipped here. 
This is a refined version of a search on ``T_VARIABLE`` token.

.. code-block:: php
   
   <?php
   
   $realVariable = 1;
   
   class foo {
       private $property;        // not a variable
       
       private function bar() {
           global $global;       // not a variable
           static $static;       // not a variable
           
       }
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/RealVariables                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


