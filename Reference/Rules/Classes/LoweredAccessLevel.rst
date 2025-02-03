.. _classes-loweredaccesslevel:


.. _lowered-access-level:

Lowered Access Level
++++++++++++++++++++


.. meta::

	:description:

		Lowered Access Level: A visibility was lowered.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Lowered Access Level

	:twitter:description: Lowered Access Level: A visibility was lowered

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Lowered Access Level

	:og:type: article

	:og:description: A visibility was lowered

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Lowered Access Level.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/LoweredAccessLevel.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/LoweredAccessLevel.html","name":"Lowered Access Level","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A visibility was lowered","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Lowered Access Level.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A visibility was lowered. While this is a PHP feature, lowering visibility means that the data is now available to more actors than previously set up, and it might yield surprises to part of the code that still rely on the previous visibility.

This applies to all visibility's structures : class constant, properties and methods.

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

Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Sync the visibility between the classes
* Use a different name for the public properties




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/LoweredAccessLevel                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


