.. _classes-tostringpss:


.. _magic-visibility:

Magic Visibility
++++++++++++++++

.. meta::
	:description:
		Magic Visibility: Magic methods must be declared with public visibility.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Magic Visibility
	:twitter:description: Magic Visibility: Magic methods must be declared with public visibility
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Magic Visibility
	:og:type: article
	:og:description: Magic methods must be declared with public visibility
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Magic Visibility.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/toStringPss.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/toStringPss.html","name":"Magic Visibility","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Magic methods must be declared with public visibility","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Magic Visibility.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Magic methods must be declared with public visibility. They cannot be private or protected.

Magic methods cannot be declared as `static <https://www.php.net/manual/en/language.oop5.static.php>`_. They are always associated with an instance of a class and cannot be called statically.

.. code-block:: php
   
   <?php
   
   class foo{
       // magic method must bt public and non-static
       public static function __clone($name) {    }
   
       // magic method can't be private
       private function __get($name) {    }
   
       // magic method can't be protected
       private function __set($name, $value) {    }
   
       // magic method can't be static
       public static function __isset($name) {    }
   }
   
   ?>

See also `Magic methods <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `PHP Magic Methods Explained <https://atakde.medium.com/php-magic-methods-explained-bac7053c007d>`_.

Related PHP errors 
-------------------

  + `The magic method x::__call() must have public visibility <https://php-errors.readthedocs.io/en/latest/messages/the-magic-method-%25s%3A%3A%25s%28%29-must-have-public-visibility.html>`_
  + `The magic method x::__get() must have public visibility <https://php-errors.readthedocs.io/en/latest/messages/the-magic-method-%25s%3A%3A%25s%28%29-must-have-public-visibility.html>`_
  + `The magic method x::__isset() must have public visibility <https://php-errors.readthedocs.io/en/latest/messages/the-magic-method-%25s%3A%3A%25s%28%29-must-have-public-visibility.html>`_
  + `The magic method x::__set() must have public visibility <https://php-errors.readthedocs.io/en/latest/messages/the-magic-method-%25s%3A%3A%25s%28%29-must-have-public-visibility.html>`_



Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_
  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/toStringPss                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


