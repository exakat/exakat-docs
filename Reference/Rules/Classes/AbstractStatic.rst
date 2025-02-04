.. _classes-abstractstatic:


.. _abstract-static-methods:

Abstract Static Methods
+++++++++++++++++++++++

.. meta::
	:description:
		Abstract Static Methods: Methods cannot be both abstract and static.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Abstract Static Methods
	:twitter:description: Abstract Static Methods: Methods cannot be both abstract and static
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Abstract Static Methods
	:og:type: article
	:og:description: Methods cannot be both abstract and static
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Abstract Static Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AbstractStatic.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AbstractStatic.html","name":"Abstract Static Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Methods cannot be both abstract and static","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Abstract Static Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Methods cannot be both abstract and `static <https://www.php.net/manual/en/language.oop5.static.php>`_. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods belong to a class, and will not be overridden by the child class. For normal methods, PHP will start at the object level, then go up the hierarchy to find the method. With `static <https://www.php.net/manual/en/language.oop5.static.php>`_, it is necessary to mention the name, or use Late `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ Binding, with `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or `static <https://www.php.net/manual/en/language.oop5.static.php>`_. Hence, it is useless to have an abstract `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method : it should be a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method.

A child class is able to declare a method with the same name than a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, but those two methods will stay independent. 

This is not the case anymore in PHP 7.0+.

.. code-block:: php
   
   <?php
   
   abstract class foo {
       // This is not possible
       static abstract function bar() ;
   }
   
   ?>

See also `Why does PHP 5.2+ disallow abstract static class methods? <https://stackoverflow.com/questions/999066/why-does-php-5-2-disallow-abstract-static-class-methods>`_.

Connex PHP features
-------------------

  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_
  + `Abstract Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_
  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Remove abstract keyword from the method
* Remove static keyword from the method
* Remove the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AbstractStatic                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


