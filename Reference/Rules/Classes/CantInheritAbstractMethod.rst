.. _classes-cantinheritabstractmethod:


.. _cant-inherit-abstract-method:

Cant Inherit Abstract Method
++++++++++++++++++++++++++++

.. meta::
	:description:
		Cant Inherit Abstract Method: Inheriting abstract methods was made available in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cant Inherit Abstract Method
	:twitter:description: Cant Inherit Abstract Method: Inheriting abstract methods was made available in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cant Inherit Abstract Method
	:og:type: article
	:og:description: Inheriting abstract methods was made available in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cant Inherit Abstract Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CantInheritAbstractMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CantInheritAbstractMethod.html","name":"Cant Inherit Abstract Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Inheriting abstract methods was made available in PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cant Inherit Abstract Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Inheriting abstract methods was made available in PHP 7.2. In previous versions, it emitted a fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   abstract class A           { abstract function bar(stdClass $x);  }
   abstract class B extends A { abstract function bar($x): stdClass; }
   
   //   Fatal error: Can't inherit abstract function A::bar()
   ?>

See also `PHP RFC: Allow abstract function override <https://wiki.php.net/rfc/allow-abstract-function-override>`_.

Related PHP errors 
-------------------

  + `Can't inherit abstract function A::bar() <https://php-errors.readthedocs.io/en/latest/messages/can%27t-inherit-abstract-function-%25s%3A%3A%25s%28%29-%28previously-declared-abstract-in-%25s%29.html>`_



Connex PHP features
-------------------

  + `Abstract Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Avoid inheriting abstract methods for compatibility beyond 7.2 (and older)




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantInheritAbstractMethod                                                                                                                                                                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.8                                                                                                                                                                                                                                                                                                                                                                                                                       |
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


