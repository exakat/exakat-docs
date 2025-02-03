.. _classes-incompatiblesignature74:

.. _incompatible-signature-methods-with-covariance:

Incompatible Signature Methods With Covariance
++++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Incompatible Signature Methods With Covariance: Methods should have the compatible signature when being overwritten.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incompatible Signature Methods With Covariance
	:twitter:description: Incompatible Signature Methods With Covariance: Methods should have the compatible signature when being overwritten
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incompatible Signature Methods With Covariance
	:og:type: article
	:og:description: Methods should have the compatible signature when being overwritten
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incompatible Signature Methods With Covariance.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/IncompatibleSignature74.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/IncompatibleSignature74.html","name":"Incompatible Signature Methods With Covariance","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Methods should have the compatible signature when being overwritten","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Incompatible Signature Methods With Covariance.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Methods should have the compatible signature when being overwritten.

The same signatures means the children class must have : 

+ the same name
+ the same visibility or less restrictive
+ the same contravariant typehint or removed
+ the same covariant return typehint or removed
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

See also `Object Inheritance <https://www.php.net/manual/en/language.oop5.inheritance.php>`_, `PHP RFC: Covariant Returns and Contravariant Parameters <https://wiki.php.net/rfc/covariant-returns-and-contravariant-parameters>`_ and :ref:`Incompatible Signature Methods <incompatible-signature-methods>`.

Related PHP errors 
-------------------

  + `Declaration of %s::%s($%s) should be compatible with %s::%s($%s = 1)  <https://php-errors.readthedocs.io/en/latest/messages/declaration-of-%25s-must-be-compatible-with-%25s.html>`_
  + `Could not check compatibility between %s::%s(%s $%s) and %s::%s(%s $%s), because class %s is not available <https://php-errors.readthedocs.io/en/latest/messages/could-not-check-compatibility-between-%25s-and-%25s%2C-because-class-%25s-is-not-available.html>`_



Connex PHP features
-------------------

  + `type-covariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-covariance.ini.html>`_
  + `type-contravariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-contravariance.ini.html>`_


Suggestions
___________

* Make signatures compatible again




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IncompatibleSignature74                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-classes-incompatiblesignature74`                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


