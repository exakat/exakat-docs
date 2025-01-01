.. _classes-multipletraitorinterface:

.. _multiple-identical-trait-or-interface:

Multiple Identical Trait Or Interface
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Identical Trait Or Interface: There is no need to use the same trait, or implements the same interface more than once in a class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Identical Trait Or Interface
	:twitter:description: Multiple Identical Trait Or Interface: There is no need to use the same trait, or implements the same interface more than once in a class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Identical Trait Or Interface
	:og:type: article
	:og:description: There is no need to use the same trait, or implements the same interface more than once in a class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/MultipleTraitOrInterface.html
	:og:locale: en
There is no need to use the same trait, or implements the same interface more than once in a class.

Up to PHP 7.4, this doesn't raise any warning. Traits are only imported once, and interfaces may be implemented as many times as wanted.

Since PHP 7.4, multiple implementations of the same interface in one class is reported at compilation time. It is possible to repeat the implementation in various levels of a class hierarchy (aka, same implements in a class and a `parent) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

This only applies in a single class: there are no checks in a class, or interface hierarchy.


.. code-block:: php
   
   <?php
   
   class foo {
       use aTrait, aTrait, aTrait;
       use aTrait;
   }
   
   class bar implements anInterface, anInterface, anInterface {
   
   }
   
   ?>

See also :ref:`Already Parents Interface <already-parents-interface>`.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Class+bar+cannot+implement+previously+implemented+interface+i.html>`_



Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Remove the duplicate trait or interface




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MultipleTraitOrInterface                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


