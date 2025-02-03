.. _classes-undefinedstaticclass:

.. _undefined-static-class:

Undefined static \:\:class
++++++++++++++++++++++++++

.. meta::
	:description:
		Undefined static ::class: The ``::class`` operator provides the full name of the class, enumeration, trait or interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined static ::class
	:twitter:description: Undefined static ::class: The ``::class`` operator provides the full name of the class, enumeration, trait or interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined static ::class
	:og:type: article
	:og:description: The ``::class`` operator provides the full name of the class, enumeration, trait or interface
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined static ::class.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedStaticclass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedStaticclass.html","name":"Undefined static ::class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The ``::class`` operator provides the full name of the class, enumeration, trait or interface","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined static ::class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The ``\:\:class`` operator provides the full name of the class, enumeration, trait or interface. ``\:\:class`` doesn't check if the corresponding class exists. 

``\:\:class`` must be checked with a call to `class_exists() <https://www.php.net/class_exists>`_. Otherwise, it may lead to a ``Class 'foo' not found`` or even silent dead code : this happens also with Catch and `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ commands with undefined classes. PHP doesn't raise an `error <https://www.php.net/error>`_ in that case.

.. code-block:: php
   
   <?php
   
   class foo() {}
   
   // prints foo
   echo foo::class; 
   
   // prints bar though bar doesn't exist.
   echo bar::class;
   
   ?>

See also `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_.

Related PHP errors 
-------------------

  + `Class '%s' not found <https://php-errors.readthedocs.io/en/latest/messages/class-%22%25s%22-not-found.html>`_
  + `Interface "%s" not found <https://php-errors.readthedocs.io/en/latest/messages/interface-%22%25s%22-not-found.html>`_
  + `Trait '%s' not found <https://php-errors.readthedocs.io/en/latest/messages/trait-%22%25s%22-not-found.html>`_
  + `Enum '%s' not found <https://php-errors.readthedocs.io/en/latest/messages/enum-%22%25s%22-not-found.html>`_



Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Create the missing class
* Fix the name part of the syntax
* Check the name part of syntax with class_exists()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedStaticclass                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


