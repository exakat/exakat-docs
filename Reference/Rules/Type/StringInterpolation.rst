.. _type-stringinterpolation:


.. _interpolation:

Interpolation
+++++++++++++

.. meta::
	:description:
		Interpolation: The following strings contain variables that are will be replaced.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Interpolation
	:twitter:description: Interpolation: The following strings contain variables that are will be replaced
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Interpolation
	:og:type: article
	:og:description: The following strings contain variables that are will be replaced
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Interpolation.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/StringInterpolation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/StringInterpolation.html","name":"Interpolation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following strings contain variables that are will be replaced","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Interpolation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following strings contain variables that are will be replaced. However, the following characters are ambiguous, and may lead to confusion. 



It is advised to add curly brackets around those structures to make them non-ambiguous.

.. code-block:: php
   
   <?php
   
   class b { 
       public $b = 'c';
       function __toString() { return __CLASS__; }
   }
   $x = array(1 => new B());
   
   // -> after the $x[1] looks like a 2nd dereferencing, but it is not. 
   print "$x[1]->b";
   // displays : b->b
   
   print "{$x[1]->b}";
   // displays : c
   
   ?>

See also `Double quoted <https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.double>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/interpolation.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/StringInterpolation                                                                                                             |
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


