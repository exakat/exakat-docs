.. _namespaces-multiplealiasdefinitions:


.. _multiple-alias-definitions:

Multiple Alias Definitions
++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Alias Definitions: Some aliases are representing different classes across the repository.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Alias Definitions
	:twitter:description: Multiple Alias Definitions: Some aliases are representing different classes across the repository
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Alias Definitions
	:og:type: article
	:og:description: Some aliases are representing different classes across the repository
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Alias Definitions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/MultipleAliasDefinitions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/MultipleAliasDefinitions.html","name":"Multiple Alias Definitions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"Some aliases are representing different classes across the repository","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Alias Definitions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some aliases are representing different classes across the repository. This leads to potential confusion. 

Across an application, it is recommended to use the same namespace for one alias. Failing to do this lead to the same keyword to represent different values in different files, with different behavior. Those are hard to find bugs.

.. code-block:: php
   
   <?php
   
   namespace A {
       use D\d; // aka D
   }
   
   // Those are usually in different files, rather than just different namespaces.
   
   namespace B {
       use B\c as D; // also D. This could be named something else
   }
   
   ?>
Connex PHP features
-------------------

  + `Namespaces <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_
  + `Naming <https://php-dictionary.readthedocs.io/en/latest/dictionary/naming.ini.html>`_
  + `Use Alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/use-alias.ini.html>`_


Suggestions
___________

* Give more specific names to classes
* Use an alias 'use A\B ac BC' to give locally another name




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/MultipleAliasDefinitions                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-namespaces-multiplealiasdefinitions`, :ref:`case-phinx-namespaces-multiplealiasdefinitions`                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


