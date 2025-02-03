.. _structures-initthenif:


.. _init-then-update:

Init Then Update
++++++++++++++++

.. meta::
	:description:
		Init Then Update: This is a structure where the variable is initialized in the main sequence of the code, then adapted to another value in a subsequent if structure.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Init Then Update
	:twitter:description: Init Then Update: This is a structure where the variable is initialized in the main sequence of the code, then adapted to another value in a subsequent if structure
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Init Then Update
	:og:type: article
	:og:description: This is a structure where the variable is initialized in the main sequence of the code, then adapted to another value in a subsequent if structure
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Init Then Update.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InitThenIf.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InitThenIf.html","name":"Init Then Update","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 03 Feb 2025 17:19:52 +0000","dateModified":"Mon, 03 Feb 2025 17:19:52 +0000","description":"This is a structure where the variable is initialized in the main sequence of the code, then adapted to another value in a subsequent if structure","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Init Then Update.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This is a structure where the variable is initialized in the main sequence of the code, then adapted to another value in a subsequent if structure.

This analysis reports such structures, based on assignation of constant values in the initial statement.

.. code-block:: php
   
   <?php
   
   $a = 1;
   if ($b === 2) {
   	$a = 2;
   }
   
   ?>
Connex PHP features
-------------------

  + `initialisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/initialisation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InitThenIf                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


