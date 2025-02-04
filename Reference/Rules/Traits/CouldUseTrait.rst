.. _traits-couldusetrait:


.. _could-use-trait:

Could Use Trait
+++++++++++++++

.. meta::
	:description:
		Could Use Trait: The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Trait
	:twitter:description: Could Use Trait: The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Trait
	:og:type: article
	:og:description: The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Trait.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/CouldUseTrait.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/CouldUseTrait.html","name":"Could Use Trait","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Trait.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code.

The comparison between the class methods' and the trait's methods are based on token. They may yield some `false <https://www.php.net/false>`_-positives.

.. code-block:: php
   
   <?php
   
   trait t {
       function t1() {}
       function t2() {}
       function t3() {}
   }
   
   // t1, t2, t3 method could be dropped, and replaced with 'use t'
   class foo1 {
       function t1() {}
       function t2() {}
       function t3() {}
   
       function j() {}
   }
   
   // foo2 is just the same as foo1
   class foo2 {
       use t;
   
       function j() {}
   }
   
   ?>

See also :ref:`Forgotten Interface <forgotten-interface>`.

Connex PHP features
-------------------

  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `Don't Repeat Yourself (DRY) <https://php-dictionary.readthedocs.io/en/latest/dictionary/dry.ini.html>`_
  + `Centralization <https://php-dictionary.readthedocs.io/en/latest/dictionary/centralization.ini.html>`_


Suggestions
___________

* Use trait, and remove duplicated code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/CouldUseTrait                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.5                                                                                                                   |
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


