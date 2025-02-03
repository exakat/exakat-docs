.. _php-mixedusage:

.. _mixed-type-usage:

Mixed Type Usage
++++++++++++++++

.. meta::
	:description:
		Mixed Type Usage: Usage of the ``mixed`` type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mixed Type Usage
	:twitter:description: Mixed Type Usage: Usage of the ``mixed`` type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mixed Type Usage
	:og:type: article
	:og:description: Usage of the ``mixed`` type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mixed Type Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MixedUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MixedUsage.html","name":"Mixed Type Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"Usage of the ``mixed`` type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mixed Type Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Usage of the ``mixed`` type. The ``mixed`` type represents all the available types. It is the same as leaving the type empty, except that the intention to use any type is now explicit.

.. code-block:: php
   
   <?php
   
   function foo() : mixed {
       switch(rand(0, 3)) {
           case 0:
               return false;
               
           case 1: 
               return 'a';
               
           case 2:
               return [];
               
           default:
               return null;
       }
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/language.types.declarations.php>`_.

Connex PHP features
-------------------

  + `mixed <https://php-dictionary.readthedocs.io/en/latest/dictionary/mixed.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MixedUsage                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


