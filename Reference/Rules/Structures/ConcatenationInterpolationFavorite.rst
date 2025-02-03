.. _structures-concatenationinterpolationfavorite:


.. _concatenation-interpolation-consistence:

Concatenation Interpolation Consistence
+++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Concatenation Interpolation Consistence: Concatenations are done with the .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Concatenation Interpolation Consistence
	:twitter:description: Concatenation Interpolation Consistence: Concatenations are done with the 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Concatenation Interpolation Consistence
	:og:type: article
	:og:description: Concatenations are done with the 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Concatenation Interpolation Consistence.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ConcatenationInterpolationFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ConcatenationInterpolationFavorite.html","name":"Concatenation Interpolation Consistence","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Concatenations are done with the ","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Concatenation Interpolation Consistence.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Concatenations are done with the . operator or by interpolation inside a string. 

Interpolation is a clean way to write concatenation, though it gets messy with long dereferences or with constants. Concatenations are longer to write. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   // be consistent
   $a = "$b $c";
   $d = "$b $e";
   $e = "$b $e";
   $d = "$b $f";
   $f = "$b $z";
   $h = "$b $e";
   $y = "$b $e";
   $d = "$b $x";
   $j = "$b $c";
   $d = "$b $g";
   $d = "$b $h"; 
   
   // Be consistent, always use the same syntax
   $z = $w.' '.$e;
   
   ?>
Connex PHP features
-------------------

  + `concatenation <https://php-dictionary.readthedocs.io/en/latest/dictionary/concatenation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConcatenationInterpolationFavorite                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


