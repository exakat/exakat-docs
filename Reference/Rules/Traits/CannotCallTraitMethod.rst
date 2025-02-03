.. _traits-cannotcalltraitmethod:


.. _cannot-call-static-trait-method-directly:

Cannot Call Static Trait Method Directly
++++++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Cannot Call Static Trait Method Directly: From the migration docs : Calling a static method, or accessing a static property directly on a trait is deprecated.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Cannot Call Static Trait Method Directly

	:twitter:description: Cannot Call Static Trait Method Directly: From the migration docs : Calling a static method, or accessing a static property directly on a trait is deprecated

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Cannot Call Static Trait Method Directly

	:og:type: article

	:og:description: From the migration docs : Calling a static method, or accessing a static property directly on a trait is deprecated

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cannot Call Static Trait Method Directly.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/CannotCallTraitMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/CannotCallTraitMethod.html","name":"Cannot Call Static Trait Method Directly","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"From the migration docs : Calling a static method, or accessing a static property directly on a trait is deprecated","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cannot Call Static Trait Method Directly.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

From the migration docs : Calling a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, or accessing a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property directly on a trait is deprecated. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods and properties should only be accessed on a class using the trait.

.. code-block:: php
   
   <?php
    trait t { static public function t() {}}
    a::t();
   // OK
    t::t();
    //Calling static trait method t::t is deprecated, it should only be called on a class using the trait
    
    class a {
       use t;
    }
   
   ?>

See also `Calling a static element on a trait  <https://www.php.net/manual/en/migration81.deprecated.php#migration81.deprecated.core.static-trait>`_.

Related PHP errors 
-------------------

  + `Calling static trait method t::t is deprecated, it should only be called on a class using the trait <https://php-errors.readthedocs.io/en/latest/messages/calling-static-trait-method-%25s%3A%3A%25s-is-deprecated.html>`_



Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `static-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-method.ini.html>`_


Suggestions
___________

* Use the trait in a class, and call the method from the class.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/CannotCallTraitMethod                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


