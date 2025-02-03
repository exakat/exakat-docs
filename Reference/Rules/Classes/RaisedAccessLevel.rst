.. _classes-raisedaccesslevel:


.. _raised-access-level:

Raised Access Level
+++++++++++++++++++

.. meta::
	:description:
		Raised Access Level: A visibility may be lowered, but not raised.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Raised Access Level
	:twitter:description: Raised Access Level: A visibility may be lowered, but not raised
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Raised Access Level
	:og:type: article
	:og:description: A visibility may be lowered, but not raised
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Raised Access Level.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/RaisedAccessLevel.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/RaisedAccessLevel.html","name":"Raised Access Level","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"A visibility may be lowered, but not raised","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Raised Access Level.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A visibility may be lowered, but not raised. Visibilities apply to properties, methods and class constants. 

This `error <https://www.php.net/error>`_ may be detected by PHP when the classes are in the same file, and declared in the right order : then, PHP reports a compilation `error <https://www.php.net/error>`_. However, when the classes are separated in different files, as it is customary, PHP won't check this at linting time, yielding a fatal `error <https://www.php.net/error>`_ at execution time.

.. code-block:: php
   
   <?php
   
   class Foo {
       public $publicProperty;
       protected $protectedProperty;
       private $privateProperty;
   }
   
   class Bar extends Foo {
       private $publicProperty;
       private $protectedProperty;
       private $privateProperty;   // This one is OK
   }
   ?>

See also `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_ and `Understanding the concept of visibility in object oriented php <https://torquemag.io/2016/05/understanding-concept-visibility-object-oriented-php/>`_.

Related PHP errors 
-------------------

  + `Access level to %s::$%s must be public (as in class %s) <https://php-errors.readthedocs.io/en/latest/messages/access-level-to-%25s%3A%3A%25s-must-be-%25s-%28as-in-%25s-%25s%29%25s.html>`_



Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Lower the visibility in the child class
* Raise the visibility in the parent class




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/RaisedAccessLevel                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.0                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


