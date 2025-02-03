.. _namespaces-unresolveduse:

.. _unresolved-use:

Unresolved Use
++++++++++++++

.. meta::
	:description:
		Unresolved Use: The following use instructions cannot be resolved to a known class, interface, trait, constant or function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unresolved Use
	:twitter:description: Unresolved Use: The following use instructions cannot be resolved to a known class, interface, trait, constant or function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unresolved Use
	:og:type: article
	:og:description: The following use instructions cannot be resolved to a known class, interface, trait, constant or function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unresolved Use.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/UnresolvedUse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/UnresolvedUse.html","name":"Unresolved Use","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following use instructions cannot be resolved to a known class, interface, trait, constant or function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unresolved Use.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The following use instructions cannot be resolved to a known class, interface, trait, constant or function. They should be dropped or fixed.

A known class, interface, trait, constant or function is defined in PHP (standard), an extension, a stub or the current code.
Use expression are options for the current namespace.

.. code-block:: php
   
   <?php
   
   namespace A {
       // class B is defined
       class B {}
       // class C is not defined
   }
   
   namespace X/Y {
   
       use A/B;  // This use is valid
       use A/C;  // This use point to nothing.
   
       new B();
       new C();
   }
   
   ?>

See also `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_.

Connex PHP features
-------------------

  + `namespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_
  + `use <https://php-dictionary.readthedocs.io/en/latest/dictionary/use.ini.html>`_


Suggestions
___________

* Remove the use expression
* Fix the use expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/UnresolvedUse                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unresolved-use <https://github.com/dseguy/clearPHP/tree/master/rules/no-unresolved-use.md>`__                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


