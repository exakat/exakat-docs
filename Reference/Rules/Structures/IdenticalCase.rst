.. _structures-identicalcase:


.. _identical-case-in-switch:

Identical Case In Switch
++++++++++++++++++++++++

.. meta::
	:description:
		Identical Case In Switch: In a switch() or match() statement, when there are identical cases, it means that multiple case labels that have the same code block.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Identical Case In Switch
	:twitter:description: Identical Case In Switch: In a switch() or match() statement, when there are identical cases, it means that multiple case labels that have the same code block
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Identical Case In Switch
	:og:type: article
	:og:description: In a switch() or match() statement, when there are identical cases, it means that multiple case labels that have the same code block
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Identical Case In Switch.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IdenticalCase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IdenticalCase.html","name":"Identical Case In Switch","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"In a switch() or match() statement, when there are identical cases, it means that multiple case labels that have the same code block","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Identical Case In Switch.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

In a `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ or `match() <https://www.php.net/manual/en/control-structures.match.php>`_ statement, when there are identical cases, it means that multiple case labels that have the same code block. 

This can happen by mistake or design. They may be merged together.

.. code-block:: php
   
   <?php
   
   switch($a) {
   	case 1: 
   		$b = 2;
   		break;
   
   	case 2: 
   		$b = 12;
   		break;
   
   	// Identical to case 1
   	case 3: 
   		$b = 2;
   		break;
   }
   
   ?>
Connex PHP features
-------------------

  + `Don't Repeat Yourself (DRY) <https://php-dictionary.readthedocs.io/en/latest/dictionary/dry.ini.html>`_


Suggestions
___________

* Merge the cases and reduce the size of code
* Review the cases code and make them different




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalCase                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


