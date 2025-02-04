.. _complete-createdefaultvalues:


.. _create-default-values:

Create Default Values
+++++++++++++++++++++

.. meta::
	:description:
		Create Default Values: This commands adds a link between variables, property definitions and any assignation to this container.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Create Default Values
	:twitter:description: Create Default Values: This commands adds a link between variables, property definitions and any assignation to this container
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Create Default Values
	:og:type: article
	:og:description: This commands adds a link between variables, property definitions and any assignation to this container
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Create Default Values.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateDefaultValues.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateDefaultValues.html","name":"Create Default Values","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"This commands adds a link between variables, property definitions and any assignation to this container","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Create Default Values.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This commands adds a link between variables, property definitions and any assignation to this container.

Variables have no definition expression in PHP. Exakat holds their definition with the `Variabledefinition` node.

Properties have definitions, and non-compulsory default values. This command creates multiple DEFINITION link for them.

DEFAULT is convenient in the case of `null` value, which will be assigned an object at execution time. 
Short assignations, such as `+=`  are not considered default value. It needs to be a full assignation

.. code-block:: php
   
   <?php
   
   function foo() {
       // local Variabledefinition links to this expression
       $a = 1;
   }
   
   class x {
       // 1 is a default value
       private $p = 1;
       
       function __construct() {
           // 2 is also a default value for this.
           // This default value is different from the above as it is a part of an assignation
           $this->p = 2;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Default Value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateDefaultValues                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
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


