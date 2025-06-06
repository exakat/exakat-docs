.. _functions-avoidbooleanargument:


.. _use-named-boolean-in-argument-definition:

Use Named Boolean In Argument Definition
++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Use Named Boolean In Argument Definition: Boolean values in argument definition are confusing.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Named Boolean In Argument Definition
	:twitter:description: Use Named Boolean In Argument Definition: Boolean values in argument definition are confusing
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Named Boolean In Argument Definition
	:og:type: article
	:og:description: Boolean values in argument definition are confusing
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Named Boolean In Argument Definition.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/AvoidBooleanArgument.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/AvoidBooleanArgument.html","name":"Use Named Boolean In Argument Definition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Boolean values in argument definition are confusing","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Named Boolean In Argument Definition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Boolean values in argument definition are confusing. 

It is recommended to use explicit constant names or enumerations, instead. They are more readable. They also allow for easy replacement when the code evolve and has to replace those booleans by strings. This works even also with classes, and class constants.

.. code-block:: php
   
   <?php
   
   function flipImage($im, $horizontal = NO_HORIZONTAL_FLIP, $vertical = NO_VERTICAL_FLIP) { }
   
   // with constants
   const HORIZONTAL_FLIP = true;
   const NO_HORIZONTAL_FLIP = true;
   const VERTICAL_FLIP = true;
   const NO_VERTICAL_FLIP = true;
   
   rotateImage($im, HORIZONTAL_FLIP, NO_VERTICAL_FLIP);
   
   // without constants 
   function flipImage($im, $horizontal = false, $vertical = false) { }
   
   rotateImage($im, true, false);
   
   ?>

See also `Improve Passing Booleans in PHP  <https://freek.dev/2227-improve-passing-booleans-in-php>`_, `Flag Argument <https://martinfowler.com/bliki/FlagArgument.html>`_ and `Improve Passing Booleans in PHP  <https://freek.dev/2227-improve-passing-booleans-in-php>`_.

Connex PHP features
-------------------

  + `Boolean <https://php-dictionary.readthedocs.io/en/latest/dictionary/boolean.ini.html>`_
  + `Argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Suggestions
___________

* Use available constants, global or class
* Create a constant, global or class, and use it
* Use named parameters to clarify the target of the boolean
* Use a single-parameter method, so that the value of the boolean is obvious
* Use an enumeration




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/AvoidBooleanArgument                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpmyadmin-functions-avoidbooleanargument`, :ref:`case-cleverstyle-functions-avoidbooleanargument`           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


