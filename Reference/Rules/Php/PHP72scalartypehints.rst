.. _php-php72scalartypehints:

.. _php-7.2-scalar-types:

PHP 7.2 Scalar Types
++++++++++++++++++++

.. meta::
	:description:
		PHP 7.2 Scalar Types: A new type was introduced : ``object``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.2 Scalar Types
	:twitter:description: PHP 7.2 Scalar Types: A new type was introduced : ``object``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.2 Scalar Types
	:og:type: article
	:og:description: A new type was introduced : ``object``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.2 Scalar Types.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PHP72scalartypehints.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PHP72scalartypehints.html","name":"PHP 7.2 Scalar Types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"A new type was introduced : ``object``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.2 Scalar Types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A new type was introduced : ``object``. 

It can't be used before PHP 7.2, and will be confused with classes or interfaces.

.. code-block:: php
   
   <?php
   
   function test(object $obj) : object
   {
       return new SplQueue();
   }
   
   test(new StdClass());
   
   ?>

See also `New object type <https://www.php.net/manual/en/migration72.new-features.php#migration72.new-features.iterable-pseudo-type>`_ and `PHP 7.2 and Object Typehint <http://blog.tekmi.nl/php-7-2-and-object-typehint/>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PHP72scalartypehints                                                                                                                                                                                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                                                                                                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and more recent                                                                                                                                                                                                                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


