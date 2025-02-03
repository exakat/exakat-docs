.. _php-yieldfromusage:

.. _yield-from-usage:

Yield From Usage
++++++++++++++++

.. meta::
	:description:
		Yield From Usage: Usage of generator delegation, with ``yield from`` keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Yield From Usage
	:twitter:description: Yield From Usage: Usage of generator delegation, with ``yield from`` keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Yield From Usage
	:og:type: article
	:og:description: Usage of generator delegation, with ``yield from`` keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Yield From Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/YieldFromUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/YieldFromUsage.html","name":"Yield From Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usage of generator delegation, with ``yield from`` keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Yield From Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Usage of `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ delegation, with ``yield from`` keyword.

In PHP 7, `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ delegation allows you to yield values from another ``Generator``, ``Traversable`` object, or array by using the ``yield from``. 

``Yield from`` was introduced in PHP 7.1, and is backward incompatible.

.. code-block:: php
   
   <?php
   
   // Yield delegation
   function foo() {
       yield from bar();
   }
   
   function bar() {
       yield 1;
   }
   
   ?>

See also `Generator Syntax <https://www.php.net/manual/en/language.generators.syntax.php>`_ and `Understanding PHP Generators <https://scotch.io/tutorials/understanding-php-generators>`_.

Connex PHP features
-------------------

  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `yield-from <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/YieldFromUsage                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


