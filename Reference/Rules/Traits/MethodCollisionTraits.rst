.. _traits-methodcollisiontraits:


.. _method-collision-traits:

Method Collision Traits
+++++++++++++++++++++++

.. meta::
	:description:
		Method Collision Traits: Two or more traits are included in the same class, and they have methods collisions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Collision Traits
	:twitter:description: Method Collision Traits: Two or more traits are included in the same class, and they have methods collisions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Collision Traits
	:og:type: article
	:og:description: Two or more traits are included in the same class, and they have methods collisions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Collision Traits.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/MethodCollisionTraits.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/MethodCollisionTraits.html","name":"Method Collision Traits","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"Two or more traits are included in the same class, and they have methods collisions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Collision Traits.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Two or more traits are included in the same class, and they have methods collisions. 

Those collisions should be solved with a ``use`` expression. When they are not, PHP stops execution with a fatal `error <https://www.php.net/error>`_ : ``Trait method M has not been applied, because there are collisions with other trait methods on C``.

The code shown lints, but doesn't execute.

.. code-block:: php
   
   <?php
   
   trait A {
       public function A() {}
       public function M() {}
   }
   
   trait B {
       public function B() {}
       public function M() {}
   }
   
   class C {
       use  A, B;
   }
   
   class D {
       use  A, B{
           B::M insteadof A;
       };
   }
   
   ?>

See also https://www.php.net/manual/en/language.oop5.traits.php.

Related PHP errors 
-------------------

  + `Trait method M has not been applied, because there are collisions with other trait methods on C <https://php-errors.readthedocs.io/en/latest/messages/trait-method-%25s%3A%3A%25s-has-not-been-applied-as-%25s%3A%3A%25s.html>`_



Connex PHP features
-------------------

  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_
  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `method-collision <https://php-dictionary.readthedocs.io/en/latest/dictionary/method-collision.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/MethodCollisionTraits                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.2                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


