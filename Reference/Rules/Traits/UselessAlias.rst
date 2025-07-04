.. _traits-uselessalias:


.. _useless-method-alias:

Useless Method Alias
++++++++++++++++++++

.. meta::
	:description:
		Useless Method Alias: It is not possible to declare an alias of a method with the same name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Method Alias
	:twitter:description: Useless Method Alias: It is not possible to declare an alias of a method with the same name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Method Alias
	:og:type: article
	:og:description: It is not possible to declare an alias of a method with the same name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Method Alias.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/UselessAlias.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/UselessAlias.html","name":"Useless Method Alias","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"It is not possible to declare an alias of a method with the same name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Method Alias.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not possible to declare an alias of a method with the same name. 

PHP reports that ``Trait method f has not been applied, because there are collisions with other trait methods on x``, which is a way to say that the alias will be in conflict with the method name. 

When the method is the only one bearing a name, and being imported, there is no need to alias it. When the method is imported in several traits, the keyword ``insteadof`` is available to solve the conflict.

This code lints but doesn't execute.

.. code-block:: php
   
   <?php
   
   trait T {
       function h() {}
       function f() {}
   }
   
   class X {
       use T { 
           // This is possible
           T::f as g; 
   
           // This is not possible, as the alias is in conflict with itself
           // alias are case insensitive
           T::f as F; 
       }
   }
   
   ?>

See also `Conflict resolution <https://www.php.net/manual/en/language.oop5.traits.php#language.oop5.traits.conflict>`_.

Related PHP errors 
-------------------

  + `Trait method M has not been applied, because there are collisions with other trait methods on X <https://php-errors.readthedocs.io/en/latest/messages/trait-method-%25s%3A%3A%25s-has-not-been-applied-as-%25s%3A%3A%25s.html>`_



Connex PHP features
-------------------

  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Remove the alias
* Fix the alias or the origin method name
* Switch to insteadof, and avoid as keyword




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UselessAlias                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.6                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


