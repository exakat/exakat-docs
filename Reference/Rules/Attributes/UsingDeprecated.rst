.. _attributes-usingdeprecated:


.. _using-deprecated-feature:

Using Deprecated Feature
++++++++++++++++++++++++

.. meta::
	:description:
		Using Deprecated Feature: Deprecated attribute marks a class, interface, trait, enumeration, function, closure, array function, parameter, as a deprecated feature.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Using Deprecated Feature
	:twitter:description: Using Deprecated Feature: Deprecated attribute marks a class, interface, trait, enumeration, function, closure, array function, parameter, as a deprecated feature
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Using Deprecated Feature
	:og:type: article
	:og:description: Deprecated attribute marks a class, interface, trait, enumeration, function, closure, array function, parameter, as a deprecated feature
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Using Deprecated Feature.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/UsingDeprecated.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/UsingDeprecated.html","name":"Using Deprecated Feature","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Deprecated attribute marks a class, interface, trait, enumeration, function, closure, array function, parameter, as a deprecated feature","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Using Deprecated Feature.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Deprecated `attribute <https://www.php.net/attribute>`_ marks a class, interface, trait, enumeration, function, `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, array function, parameter, as a deprecated feature. This rule reports usage of these structure, so they can be removed.

Note that the class ` :ref:`rulesets-deprecated` ` does not need to be defined anywhere.

.. code-block:: php
   
   <?php
   
   #[Deprecated]
   function foo() { }
   
   // This is reported
   foo(); 
   
   ?>
Connex PHP features
-------------------

  + `Attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Suggestions
___________

* Remove usage of this deprecated feature, so they can be removed ultimately.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/UsingDeprecated                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


