.. _complete-createforeachdefault:


.. _create-foreach-default:

Create Foreach Default
++++++++++++++++++++++

.. meta::
	:description:
		Create Foreach Default: This command adds DEFAULT link from the blind variables to the literal definitions, when they are available.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Create Foreach Default
	:twitter:description: Create Foreach Default: This command adds DEFAULT link from the blind variables to the literal definitions, when they are available
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Create Foreach Default
	:og:type: article
	:og:description: This command adds DEFAULT link from the blind variables to the literal definitions, when they are available
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Create Foreach Default.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateForeachDefault.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateForeachDefault.html","name":"Create Foreach Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"This command adds DEFAULT link from the blind variables to the literal definitions, when they are available","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Create Foreach Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command adds DEFAULT link from the blind variables to the literal definitions, when they are available. This adds sources for `static <https://www.php.net/manual/en/language.oop5.static.php>`_ loops, which are based on hardcoded list of data. Dynamic loops are not affected.

.. code-block:: php
   
   <?php
   
   // $a may b e 1, 2 or 3
   foreach([1,2,3] as $a) {
       echo $a;
   }
   
   ?>
Connex PHP features
-------------------

  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateForeachDefault                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


