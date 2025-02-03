.. _classes-abstractorimplements:


.. _abstract-or-implements:

Abstract Or Implements
++++++++++++++++++++++


.. meta::

	:description:

		Abstract Or Implements: A class must implements all abstract methods of it parents, or be abstract too.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Abstract Or Implements

	:twitter:description: Abstract Or Implements: A class must implements all abstract methods of it parents, or be abstract too

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Abstract Or Implements

	:og:type: article

	:og:description: A class must implements all abstract methods of it parents, or be abstract too

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Abstract Or Implements.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AbstractOrImplements.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AbstractOrImplements.html","name":"Abstract Or Implements","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"A class must implements all abstract methods of it parents, or be abstract too","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Abstract Or Implements.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A class must implements all abstract methods of it parents, or be abstract too. 

PHP detect such `error <https://www.php.net/error>`_ when all classes are loaded: in a code source where classes are split by files, such `error <https://www.php.net/error>`_ it won't be detected until execution, where PHP stops with a Fatal `Error <https://www.php.net/error>`_ : ``Class BA contains 1 abstract method and must therefore be declared abstract or implement the remaining methods (A\:\:aFoo)``.

.. code-block:: php
   
   <?php
   
   abstract class Foo { 
       abstract function FooBar();
   }
   
   // This is in another file : php -l would detect it right away
   
   class FooFoo extends Foo { 
       // The method is not defined. 
       // The class must be abstract, just like Foo
   }
   
   ?>

See also `Class Abstraction <https://www.php.net/abstract>`_.

Related PHP errors 
-------------------

  + `Class %s contains 1 abstract method and must therefore be declared abstract or implement the remaining methods (%s::%s) <https://php-errors.readthedocs.io/en/latest/messages/class-%25s-contains-%25d-abstract-method%25s-and-must-therefore-be-declared-abstract-or-implement-the-remaining-methods.html>`_



Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_
  + `implements <https://php-dictionary.readthedocs.io/en/latest/dictionary/implements.ini.html>`_
  + `lazy-loading <https://php-dictionary.readthedocs.io/en/latest/dictionary/lazy-loading.ini.html>`_


Suggestions
___________

* Implements all the abstract methods of the class
* Make the class abstract




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AbstractOrImplements                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-classes-abstractorimplements`                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


