.. _traits-alreadyparentstrait:


.. _already-parents-trait:

Already Parents Trait
+++++++++++++++++++++

.. meta::
	:description:
		Already Parents Trait: Trait is already used a parent's class or trait.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Already Parents Trait
	:twitter:description: Already Parents Trait: Trait is already used a parent's class or trait
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Already Parents Trait
	:og:type: article
	:og:description: Trait is already used a parent's class or trait
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Already Parents Trait.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/AlreadyParentsTrait.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/AlreadyParentsTrait.html","name":"Already Parents Trait","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Trait is already used a parent's class or trait","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Already Parents Trait.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Trait is already used a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s class or trait. There is no use to include it a second time, so one of them can be removed.

.. code-block:: php
   
   <?php
   
   trait ta {
       use tb;
   }
   
   trait t1 {
       use ta;
       use tb; // also used by ta
   }
   
   class b {
       use t1; // also required by class c
       use ta; // also required by trait t1
   }
   
   class c extends b {
       use t1;
   }
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Connex PHP features
-------------------

  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Eliminate the trait in the parent class
* Eliminate the trait in the child class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/AlreadyParentsTrait                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                   |
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


