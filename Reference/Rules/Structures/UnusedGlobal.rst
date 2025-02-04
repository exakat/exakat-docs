.. _structures-unusedglobal:


.. _unused-global:

Unused Global
+++++++++++++

.. meta::
	:description:
		Unused Global: A global keyword is used in a method, yet the variable is not actually used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Global
	:twitter:description: Unused Global: A global keyword is used in a method, yet the variable is not actually used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Global
	:og:type: article
	:og:description: A global keyword is used in a method, yet the variable is not actually used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Global.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnusedGlobal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnusedGlobal.html","name":"Unused Global","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A global keyword is used in a method, yet the variable is not actually used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Global.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A global keyword is used in a method, yet the variable is not actually used. This makes PHP import values for nothing, or may create interference

.. code-block:: php
   
   <?php
       function foo() {
           global bar;
           
           return 1;
       }
   ?>
Connex PHP features
-------------------

  + `global Scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_
  + `Unused <https://php-dictionary.readthedocs.io/en/latest/dictionary/unused.ini.html>`_


Suggestions
___________

* Remove the global declaration
* Remove the global variable altogether




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnusedGlobal                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-structures-unusedglobal`                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


