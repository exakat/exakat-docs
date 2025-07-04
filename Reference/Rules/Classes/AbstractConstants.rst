.. _classes-abstractconstants:


.. _abstract-class-constants:

Abstract Class Constants
++++++++++++++++++++++++

.. meta::
	:description:
		Abstract Class Constants: Those are class constants which are defined in multiple children, but not in the parent class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Abstract Class Constants
	:twitter:description: Abstract Class Constants: Those are class constants which are defined in multiple children, but not in the parent class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Abstract Class Constants
	:og:type: article
	:og:description: Those are class constants which are defined in multiple children, but not in the parent class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Abstract Class Constants.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AbstractConstants.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AbstractConstants.html","name":"Abstract Class Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those are class constants which are defined in multiple children, but not in the parent class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Abstract Class Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those are class constants which are defined in multiple children, but not in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class.

If this class is a feature of the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, or shall and must be defined in the children classes, it is recommended to add them in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, and let them overloaded in the children class.

In the illustration below, ``CONSTA`` is defined in all two children, but not in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. A third children would miss the constants definitions, until an `error <https://www.php.net/error>`_ has been reported.

.. code-block:: php
   
   <?php
   
   class A {
       // no constant
   }
   
   class A1 extends A {
       public const CONSTA = 1;
   }
   
   class A2 extends A {
       public const CONSTA = 2;
   }
   
   ?>

+---------+---------+---------+--------------------------------------------------------------------------------------------+
| Name    | Default | Type    | Description                                                                                |
+---------+---------+---------+--------------------------------------------------------------------------------------------+
| minimum | 2       | integer | Minimal number of constant found in children to report this as a potential abstract class. |
+---------+---------+---------+--------------------------------------------------------------------------------------------+



See also `I often find myself wishing for abstract constants in PHP <https://twitter.com/coderabbi/status/1480193789834760193>`_.

Connex PHP features
-------------------

  + `Static Constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_
  + `Abstract Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Define the constants in the parent class, with some neutral value




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AbstractConstants                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


