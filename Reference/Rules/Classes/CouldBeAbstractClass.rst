.. _classes-couldbeabstractclass:


.. _could-be-abstract-class:

Could Be Abstract Class
+++++++++++++++++++++++


.. meta::

	:description:

		Could Be Abstract Class: An abstract class is never instantiated, and has children class that are.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Could Be Abstract Class

	:twitter:description: Could Be Abstract Class: An abstract class is never instantiated, and has children class that are

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Could Be Abstract Class

	:og:type: article

	:og:description: An abstract class is never instantiated, and has children class that are

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Abstract Class.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeAbstractClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeAbstractClass.html","name":"Could Be Abstract Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"An abstract class is never instantiated, and has children class that are","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Abstract Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

An abstract class is never instantiated, and has children class that are. As such, a '`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_' class that is never instantiated by itself, but has its own children instantiated could be marked as abstract. 

That will prevent new code to try to instantiate it.

.. code-block:: php
   
   <?php
   
   // Example code would actually be split over multiple files.
   
   // That class could be abstract
   class motherClass {}
   
   // Those classes shouldn't be abstract
   class firstChildren extends motherClass {}
   class secondChildren extends motherClass {}
   class thirdChildren extends motherClass {}
   
   new firstChildren();
   new secondChildren();
   new thirdChildren();
   
   //Not a single : new motherClass()
   
   ?>

See also `Class Abstraction <https://www.php.net/abstract>`_ and `Abstract classes and methods <https://phpenthusiast.com/object-oriented-php-tutorials/abstract-classes-and-methods>`_.

Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Make this class an abstract class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeAbstractClass                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-edusoho-classes-couldbeabstractclass`, :ref:`case-shopware-classes-couldbeabstractclass`                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


