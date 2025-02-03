.. _attributes-missingoverridemethod:


.. _missing-overriden-method:

Missing Overriden Method
++++++++++++++++++++++++


.. meta::

	:description:

		Missing Overriden Method: This rule reports methods which bears the override attribute, but cannot have an eponymous method in the parent class.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Missing Overriden Method

	:twitter:description: Missing Overriden Method: This rule reports methods which bears the override attribute, but cannot have an eponymous method in the parent class

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Missing Overriden Method

	:og:type: article

	:og:description: This rule reports methods which bears the override attribute, but cannot have an eponymous method in the parent class

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Overriden Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/MissingOverrideMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/MissingOverrideMethod.html","name":"Missing Overriden Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"This rule reports methods which bears the override attribute, but cannot have an eponymous method in the parent class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Missing Overriden Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports methods which bears the `override <https://www.php.net/override>`_ `attribute <https://www.php.net/attribute>`_, but cannot have an eponymous method in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class.

This happens when the class has no `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, or when a trait is used in class without `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

As such, an `error <https://www.php.net/error>`_ will be raised when the class is used.

.. code-block:: php
   
   <?php
   
   class X {
       // no foo() method
   }
   
   class Y extends X {
       #[Override]
       function foo() { return 1; }
   }
   ?>
Connex PHP features
-------------------

  + `override <https://php-dictionary.readthedocs.io/en/latest/dictionary/override.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/MissingOverrideMethod                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


