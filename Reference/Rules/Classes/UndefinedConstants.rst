.. _classes-undefinedconstants:


.. _undefined-class-constants:

Undefined Class Constants
+++++++++++++++++++++++++


.. meta::

	:description:

		Undefined Class Constants: Class constants that are used, but never defined.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Undefined Class Constants

	:twitter:description: Undefined Class Constants: Class constants that are used, but never defined

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Undefined Class Constants

	:og:type: article

	:og:description: Class constants that are used, but never defined

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Class Constants.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedConstants.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedConstants.html","name":"Undefined Class Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Class constants that are used, but never defined","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined Class Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Class constants that are used, but never defined. This yield a fatal `error <https://www.php.net/error>`_ upon execution, but no feedback at compile level.

This analysis takes into account native PHP class constants, extensions and stubs. It also disambiguate enumeration cases. 

Constants are searched in the typed class or interface, and their `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_. They are not searched in the children, since the children are not necessarily available, unless the class is abstract. In particular, one of the children may not define the constant, and when such child is used, it will satisfy the type, but not the constant definition.

.. code-block:: php
   
   <?php
   
   class foo {
       const A = 1;
   }
   
   function foo(Foo $f) {
   	// here, C is not defined in the code and is reported
   	echo foo::A.foo::B.foo::C;
   	
   	// This is also an undefined constant
   	echo $f::B; 
   }
   
   ?>

See also `Class constants <https://www.php.net/manual/en/language.oop5.constants.php>`_.

Related PHP errors 
-------------------

  + `Undefined constant <https://php-errors.readthedocs.io/en/latest/messages/undefined-constant-%22%25s.html>`_



Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_
  + `undefined <https://php-dictionary.readthedocs.io/en/latest/dictionary/undefined.ini.html>`_


Suggestions
___________

* Fix the name of the constant
* Add the constant to the current class or one of its parent
* Update the constant's visibility




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedConstants                                                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


