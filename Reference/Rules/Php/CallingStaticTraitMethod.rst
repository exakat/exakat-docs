.. _php-callingstatictraitmethod:

.. _calling-static-trait-method:

Calling Static Trait Method
+++++++++++++++++++++++++++

.. meta::
	:description:
		Calling Static Trait Method: Calling directly a static method, defined in a trait is deprecated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Calling Static Trait Method
	:twitter:description: Calling Static Trait Method: Calling directly a static method, defined in a trait is deprecated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Calling Static Trait Method
	:og:type: article
	:og:description: Calling directly a static method, defined in a trait is deprecated
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Calling Static Trait Method.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CallingStaticTraitMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CallingStaticTraitMethod.html","name":"Calling Static Trait Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Calling directly a static method, defined in a trait is deprecated","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Calling Static Trait Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Calling directly a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, defined in a trait is deprecated. It emits a deprecation notice in PHP 8.1.
Calling the same method, from the class point of view is valid.

.. code-block:: php
   
   <?php
   
   trait T {
       public static function t() {
           //
       }
   }
   
   T::t();
   
   ?>

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Related PHP errors 
-------------------

  + `Calling static trait method Test::test is deprecated, it should only be called on a class using the trait <https://php-errors.readthedocs.io/en/latest/messages/calling-static-trait-method-%25s%3A%3A%25s-is-deprecated.html>`_



Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `static-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-method.ini.html>`_


Suggestions
___________

* Call the method from one of the class using the trait
* Move the method to a class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CallingStaticTraitMethod                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.5                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


