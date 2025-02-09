.. _structures-plusegalone:


.. _no-plus-one:

No Plus One
+++++++++++

.. meta::
	:description:
		No Plus One: Incrementing a variable should be done with the ++ or -- operators.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Plus One
	:twitter:description: No Plus One: Incrementing a variable should be done with the ++ or -- operators
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Plus One
	:og:type: article
	:og:description: Incrementing a variable should be done with the ++ or -- operators
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Plus One.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PlusEgalOne.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PlusEgalOne.html","name":"No Plus One","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Incrementing a variable should be done with the ++ or -- operators","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Plus One.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Incrementing a variable should be done with the ++ or -- operators. Any other way, may be avoided.



This is a micro optimisation.

.. code-block:: php
   
   <?php
   
   // Best way to increment
   ++$x; --$y;
   
   // Second best way to increment, if the current value is needed :
   echo $x++, $y--;
   
   // Good but slow 
   $x += 1; 
   $x -= -1; 
   
   $y += -1;
   $y -= 1;
   
   // even slower
   $x = $x + 1; 
   $y = $y - 1; 
   
   ?>

Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PlusEgalOne                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


