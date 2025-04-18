.. _classes-incompatiblesignature:


.. _incompatible-signature-methods:

Incompatible Signature Methods
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Incompatible Signature Methods: Methods should have the same signature when being overwritten.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incompatible Signature Methods
	:twitter:description: Incompatible Signature Methods: Methods should have the same signature when being overwritten
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incompatible Signature Methods
	:og:type: article
	:og:description: Methods should have the same signature when being overwritten
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incompatible Signature Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/IncompatibleSignature.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/IncompatibleSignature.html","name":"Incompatible Signature Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Methods should have the same signature when being overwritten","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Incompatible Signature Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Methods should have the same signature when being overwritten.

The same signatures means the children class must have : 

+ the same name
+ the same visibility or less restrictive
+ the same typehint or removed
+ the same default value or removed
+ a reference like its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_

This problem emits a fatal `error <https://www.php.net/error>`_, for abstract methods, or a warning `error <https://www.php.net/error>`_, for normal methods. Yet, it is difficult to lint, because classes are often stored in different files. As such, PHP do lint each file independently, as unknown `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes are not checked if not present. Yet, when executing the code, PHP lint the actual code and may encounter a fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   class a {
       public function foo($a = 1) {}
   }
   
   class ab extends a {
       // foo is overloaded and now includes a default value for $a
       public function foo($a) {}
   }
   
   ?>

See also `Object Inheritance <https://www.php.net/manual/en/language.oop5.inheritance.php>`_.

Related PHP errors 
-------------------

  + `Declaration of %s::%s($%s) should be compatible with %s::%s($%s = 1)  <https://php-errors.readthedocs.io/en/latest/messages/declaration-of-%25s-must-be-compatible-with-%25s.html>`_




Suggestions
___________

* Make signatures compatible again




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IncompatibleSignature                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-classes-incompatiblesignature`                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


