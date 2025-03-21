.. _classes-couldbestringable:


.. _could-be-stringable:

Could Be Stringable
+++++++++++++++++++

.. meta::
	:description:
		Could Be Stringable: ``Stringable`` is an interface that marks classes with a custom method to cast the object as a string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Stringable
	:twitter:description: Could Be Stringable: ``Stringable`` is an interface that marks classes with a custom method to cast the object as a string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Stringable
	:og:type: article
	:og:description: ``Stringable`` is an interface that marks classes with a custom method to cast the object as a string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Stringable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeStringable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeStringable.html","name":"Could Be Stringable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"``Stringable`` is an interface that marks classes with a custom method to cast the object as a string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Stringable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``Stringable`` is an interface that marks classes with a custom method to cast the object as a string. It was introduced in PHP 8.0.

Classes that defined a `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ magic method may be turned into a string when the typehint, argument, return or property, requires it. This is not the case when strict_types is activated. Yet, until PHP 8.0, there was nothing to identify a class as such.

.. code-block:: php
   
   <?php 
   
   // This class may implement Stringable
   class x {
       function __tostring() {
           return 'asd';
       }
   }
   
   echo (new x);
   
   ?>

See also `PHP RFC: Add Stringable interface <https://wiki.php.net/rfc/stringable>`_ and `The Stringable interface <https://www.php.net/manual/en/class.stringable.php>`_.

Connex PHP features
-------------------

  + `Stringable <https://php-dictionary.readthedocs.io/en/latest/dictionary/stringable.ini.html>`_
  + `String <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `Magic Methods <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Add implements stringable to the class definition
* Add extends stringable to the interface definition




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeStringable                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


