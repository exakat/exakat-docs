.. _php-globalsvsglobal:


.. _$globals-or-global:

$GLOBALS Or global
++++++++++++++++++

.. meta::
	:description:
		$GLOBALS Or global: Usually, PHP projects make a choice between the global keyword, and the $GLOBALS variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: $GLOBALS Or global
	:twitter:description: $GLOBALS Or global: Usually, PHP projects make a choice between the global keyword, and the $GLOBALS variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: $GLOBALS Or global
	:og:type: article
	:og:description: Usually, PHP projects make a choice between the global keyword, and the $GLOBALS variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/$GLOBALS Or global.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/GlobalsVsGlobal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/GlobalsVsGlobal.html","name":"$GLOBALS Or global","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usually, PHP projects make a choice between the global keyword, and the $GLOBALS variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/$GLOBALS Or global.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Usually, PHP projects make a choice between the global keyword, and the $GLOBALS variable. Sometimes, the project has no recommendations. 

When your project use a vast majority of one of the convention, then the analyzer will report all remaining inconsistently cased constant.

.. code-block:: php
   
   <?php
   
   global $a, $b, $c, $d, $e, $f, $g, $h, $i, $j, $k, $l, $m;
   
   // This access is inconsistent with the previous usage
   $GLOBALS['a'] = 2;
   
   ?>
Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/GlobalsVsGlobal                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.2                                                                                                                   |
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


