.. _structures-identicalelseif:


.. _identical-elseif:

Identical Elseif
++++++++++++++++


.. meta::

	:description:

		Identical Elseif: In a long if/elseif/then structures, identical conditions are mutually exclusive.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Identical Elseif

	:twitter:description: Identical Elseif: In a long if/elseif/then structures, identical conditions are mutually exclusive

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Identical Elseif

	:og:type: article

	:og:description: In a long if/elseif/then structures, identical conditions are mutually exclusive

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Identical Elseif.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IdenticalElseif.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IdenticalElseif.html","name":"Identical Elseif","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"In a long if\/elseif\/then structures, identical conditions are mutually exclusive","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Identical Elseif.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

In a long if/elseif/then structures, identical conditions are mutually exclusive. The first one will happen, and the second will be ignored. 

This is similar to having multiple cases in the same switch or match expression.

.. code-block:: php
   
   <?php
   
   if ($a === 1) { }
   elseif ($a === 2) { }
   elseif ($a === 3) { }
   elseif ($a === 4) { }
   elseif ($a === 2) { }
   else {}
   
   ?>
Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Remove the extra elseif() clause
* Fixed the condition of the extra elseif() clause
* Use a switch() or match() expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalElseif                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.7                                                                                                                   |
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


