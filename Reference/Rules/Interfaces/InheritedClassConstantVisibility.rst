.. _interfaces-inheritedclassconstantvisibility:


.. _inherited-class-constant-visibility:

Inherited Class Constant Visibility
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Inherited Class Constant Visibility: Visibility of class constant must be public, even when overwritten.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inherited Class Constant Visibility
	:twitter:description: Inherited Class Constant Visibility: Visibility of class constant must be public, even when overwritten
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inherited Class Constant Visibility
	:og:type: article
	:og:description: Visibility of class constant must be public, even when overwritten
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Inherited Class Constant Visibility.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/InheritedClassConstantVisibility.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/InheritedClassConstantVisibility.html","name":"Inherited Class Constant Visibility","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 22 Jan 2025 05:38:57 +0000","dateModified":"Wed, 22 Jan 2025 05:38:57 +0000","description":"Visibility of class constant must be public, even when overwritten","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Inherited Class Constant Visibility.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Visibility of class constant must be public, even when overwritten. 

This was not checked until PHP 8.3, where it is now a Fatal `Error <https://www.php.net/error>`_. When the interface and the class are defined in different files, the `error <https://www.php.net/error>`_ appears at execution time.

.. code-block:: php
   
   <?php
   
   interface i {
   	public const I = 1;
   	public const J = 2;
   }
   
   class x implements i {
   	// This should not be possible
   	private const I = 10;
   	public const J = 20;
   }
   
   ?>
Related PHP errors 
-------------------

  + `Access level to x::I must be public (as in interface i) <https://php-errors.readthedocs.io/en/latest/messages/cannot-inherit-previously-inherited-or-override-constant-%25s-from-interface-%25s.html>`_



Connex PHP features
-------------------

  + `Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_
  + `Lazy Loading <https://php-dictionary.readthedocs.io/en/latest/dictionary/lazy-loading.ini.html>`_


Suggestions
___________

* Set the constant visibility in the class to public
* Remove the visibility of the constant in the class
* Remove the implementation of the interface in the class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/InheritedClassConstantVisibility                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`, :ref:`CompatibilityPHP83 <ruleset-CompatibilityPHP83>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | 8.2                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


