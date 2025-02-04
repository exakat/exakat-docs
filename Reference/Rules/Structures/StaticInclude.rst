.. _structures-staticinclude:


.. _static-inclusions:

Static Inclusions
+++++++++++++++++

.. meta::
	:description:
		Static Inclusions: This rule reports all static inclusion.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Inclusions
	:twitter:description: Static Inclusions: This rule reports all static inclusion
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Inclusions
	:og:type: article
	:og:description: This rule reports all static inclusion
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Inclusions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StaticInclude.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StaticInclude.html","name":"Static Inclusions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule reports all static inclusion","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Inclusions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports all `static <https://www.php.net/manual/en/language.oop5.static.php>`_ inclusion. A inclusion is `static <https://www.php.net/manual/en/language.oop5.static.php>`_ when it relies only on constants, such as literals, global and class constants, and the magic constants.

This rule is a collaboration with `Bohuslav Šimek <https://twitter.`com <https://www.php.net/com>`_/BohuslavSimek>`_.

.. code-block:: php
   
   <?php
   
   // a static inclusion
   include __DIR__.'/lib/source.php';
   
   $include = '/lib/helpers.inc';
   include $include;
   
   ?>
Connex PHP features
-------------------

  + `include <https://php-dictionary.readthedocs.io/en/latest/dictionary/include.ini.html>`_
  + `Static Expression <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-expression.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StaticInclude                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.7                                                                                                                   |
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


