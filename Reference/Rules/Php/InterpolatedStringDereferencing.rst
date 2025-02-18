.. _php-interpolatedstringdereferencing:


.. _interpolated-string-dereferencing:

Interpolated String Dereferencing
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Interpolated String Dereferencing: This rule reports usage of interpolated strings (aka, strings with contain variables, with double quotes) directly, with bracket syntax.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Interpolated String Dereferencing
	:twitter:description: Interpolated String Dereferencing: This rule reports usage of interpolated strings (aka, strings with contain variables, with double quotes) directly, with bracket syntax
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Interpolated String Dereferencing
	:og:type: article
	:og:description: This rule reports usage of interpolated strings (aka, strings with contain variables, with double quotes) directly, with bracket syntax
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Interpolated String Dereferencing.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/InterpolatedStringDereferencing.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/InterpolatedStringDereferencing.html","name":"Interpolated String Dereferencing","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 18 Feb 2025 18:23:29 +0000","dateModified":"Tue, 18 Feb 2025 18:23:29 +0000","description":"This rule reports usage of interpolated strings (aka, strings with contain variables, with double quotes) directly, with bracket syntax","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Interpolated String Dereferencing.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports usage of interpolated strings (aka, strings with contain variables, with double quotes) directly, with bracket syntax.

.. code-block:: php
   
   <?php
   
   $bar = BAR
   echo foo$bar[5]; // R
   
   ?>
Connex PHP features
-------------------

  + `Interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/interpolation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/InterpolatedStringDereferencing                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | none                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                                                                   |
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


