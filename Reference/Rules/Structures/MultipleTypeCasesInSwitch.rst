.. _structures-multipletypecasesinswitch:


.. _multiple-type-cases-in-switch:

Multiple Type Cases In Switch
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Type Cases In Switch: This reports switch() instructions, which have several types in cases.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Type Cases In Switch
	:twitter:description: Multiple Type Cases In Switch: This reports switch() instructions, which have several types in cases
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Type Cases In Switch
	:og:type: article
	:og:description: This reports switch() instructions, which have several types in cases
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Type Cases In Switch.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MultipleTypeCasesInSwitch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MultipleTypeCasesInSwitch.html","name":"Multiple Type Cases In Switch","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This reports switch() instructions, which have several types in cases","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Type Cases In Switch.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This reports `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ instructions, which have several types in cases.

This might generate compatibility errors, as the comparison may succeed in different ways, depending on PHP versions. This is particularly the case for PHP 8.0, and values such as '0', '', 0, `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, and `false <https://www.php.net/false>`_.
This situation doesn't affect `match() <https://www.php.net/manual/en/control-structures.match.php>`_, as it uses a strict type comparison, unlike `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_.

.. code-block:: php
   
   <?php
   
   switch($a) {
   	case 1: 
   		break;
   		
   	case 'a':
   		break;
   }
   
   ?>
Connex PHP features
-------------------

  + `Switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_


Suggestions
___________

* Make all the types identical in the cases. 
* Switch to match() call, to include a type check




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleTypeCasesInSwitch                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


