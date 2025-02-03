.. _type-stringwithstrangespace:

.. _strings-with-strange-space:

Strings With Strange Space
++++++++++++++++++++++++++

.. meta::
	:description:
		Strings With Strange Space: An invisible space may be mistaken for a normal space.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strings With Strange Space
	:twitter:description: Strings With Strange Space: An invisible space may be mistaken for a normal space
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strings With Strange Space
	:og:type: article
	:og:description: An invisible space may be mistaken for a normal space
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strings With Strange Space.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/StringWithStrangeSpace.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/StringWithStrangeSpace.html","name":"Strings With Strange Space","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"An invisible space may be mistaken for a normal space","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Strings With Strange Space.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>An invisible space may be mistaken for a normal space. 

However, PHP does straight comparisons, and may fail at recognizing. This analysis reports when it finds such strange spaces inside strings.

PHP doesn't mistake space and tables for whitespace when tokenizing the code.

This analysis doesn't report Unicode Codepoint Notation : those are visible in the code.

.. code-block:: php
   
   <?php
   
   // PHP 7 notation, 
   $a = "\u{3000}";
   $b = " ";
   
   // Displays false
   var_dump($a === $b);
   
   ?>

See also `Unicode spaces <https://www.cs.tut.fi/~jkorpela/chars/spaces.html>`_ and `disallow irregular whitespace (no-irregular-whitespace) <http://eslint.org/docs/rules/no-irregular-whitespace>`_.

Connex PHP features
-------------------

  + `non-breakable-space <https://php-dictionary.readthedocs.io/en/latest/dictionary/non-breakable-space.ini.html>`_


Suggestions
___________

* Replace the odd spaces with a normal space
* If unsecable spaces are important for presentation, add them at the templating level.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/StringWithStrangeSpace                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-type-stringwithstrangespace`, :ref:`case-thelia-type-stringwithstrangespace`                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


