.. _complete-createcompactvariables:


.. _create-compact-variables:

Create Compact Variables
++++++++++++++++++++++++

.. meta::
	:description:
		Create Compact Variables: This command creates Variable definitions, based on usage of compact().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Create Compact Variables
	:twitter:description: Create Compact Variables: This command creates Variable definitions, based on usage of compact()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Create Compact Variables
	:og:type: article
	:og:description: This command creates Variable definitions, based on usage of compact()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Create Compact Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateCompactVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateCompactVariables.html","name":"Create Compact Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command creates Variable definitions, based on usage of compact()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Create Compact Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command creates Variable definitions, based on usage of `compact() <https://www.php.net/compact>`_. 
This only works when `compact() <https://www.php.net/compact>`_ is used with literal values, or with constants. Dynamic values are not reported.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = 1;
       return compact('a');
   }
   ?>
Connex PHP features
-------------------

  + `compact <https://php-dictionary.readthedocs.io/en/latest/dictionary/compact.ini.html>`_
  + `dynamic-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-variable.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateCompactVariables                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


